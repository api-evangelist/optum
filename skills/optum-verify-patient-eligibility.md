---
name: Verify patient eligibility and benefits
description: Check a patient's medical coverage and benefits at a payer through Optum's X12 270/271 eligibility API, in JSON or native X12, and fall back to coverage discovery when the payer or member ID is unknown.
api: openapi/optum-medical-network-eligibility-v3-openapi.yml
operations: [medicalEligibility, rawX12, healthCheck, getPayers, getOutages, postEligibility, postDiscovery, getDiscoveryById]
generated: '2026-08-14'
method: generated
---

# Verify patient eligibility and benefits

Optum's eligibility API is an X12 270/271 transaction wearing a JSON coat. Everything below is
grounded in operationIds that exist verbatim in the harvested specs.

## Before you call

1. **Get a token.** OAuth2 client-credentials only. POST `client_id` + `client_secret` to
   `https://apigw.optum.com/apip/auth/v2/token` (Medical Network APIs) — the newer Optum Real
   `oihub` APIs use `/apip/auth/sntl/v1/token` instead. The token is a JWT valid for 3600 seconds;
   send it as `Authorization: Bearer <access_token>` over TLS 1.2+. See
   `../authentication/optum-authentication.yml`.
2. **Resolve the payer.** Do not guess `tradingPartnerServiceId`. Call `getPayers`
   (`openapi/optum-payer-list-api-v1-openapi.yml`) and match the payer, then check `getOutages`
   from the same spec — Optum publishes live payer connectivity outages, and submitting into an
   outage produces a failure that looks like a data error.
3. **Pick your environment by host.** `https://sandbox-apigw.optum.com` is canned-response test;
   `https://apigw.optum.com` is live. There is no key prefix to tell them apart. Several operations
   also require an `environment` header. See `../sandbox/optum-sandbox.yml`.

## The happy path

- `medicalEligibility` — `POST /medicalnetwork/eligibility/v3/`. JSON in, JSON out. This is the
  270 inquiry and the 271 response, mapped to named fields
  (`benefitsInformation`, `benefitsRelatedEntities`, `eligibilityAdditionalInformationList`).
- `rawX12` — `POST /medicalnetwork/eligibility/v3/raw-x12`. Same transaction if you already hold a
  270. Use this when you are bridging an existing EDI pipeline; use the JSON form otherwise.
- `healthCheck` — `GET /medicalnetwork/eligibility/v3/healthcheck`. Poll before a batch run.
  status.optum.com is product-level ("Medical Network"), not endpoint-level.

## When coverage is unknown

If you do not know which payer covers the patient, switch to the Enhanced Eligibility API
(`openapi/optum-enhanced-eligibility-api-openapi.yml`) — the only Optum spec that declares the
production host:

- `postDiscovery` — `POST /rcm/eligibility/v1/coverage-discovery`. **Asynchronous.** Supply a
  `callbackUrl` in the body and Optum POSTs the completed `CoverageDiscoveryTask` back to it,
  expecting a `204 No Content`.
- `getDiscoveryById` — `GET /rcm/eligibility/v1/coverage-discovery/{id}`. The polling alternative,
  returning the same model. Prefer this if you cannot expose a public callback endpoint.
- `postEligibility` — `POST /rcm/eligibility/v1` for the synchronous enhanced inquiry.

The callback carries **no signature and no shared secret** (`../asyncapi/optum-webhooks.yml`). You
cannot verify a delivery came from Optum, so treat the callback as a hint and re-read the task with
`getDiscoveryById` before acting on it.

## Rules an agent must not break

- **There is no idempotency key.** Nothing on this platform accepts `Idempotency-Key`
  (`../conventions/optum-conventions.yml`). A timed-out eligibility inquiry is safe to retry; a
  timed-out *claim submission* is not — see the claim-submission skill.
- **Never send real PHI to the sandbox.** The docs are explicit: "Do not use real-world values in
  our sandbox API endpoints" and "Do not submit PHI or PII data in the sandbox environment." The
  sandbox only resolves predefined canned patient and provider values.
- **Read the X12 acknowledgement, not just the HTTP status.** A 200 means Optum accepted the
  transaction, not that the payer did.
- **Budget blind.** Optum publishes no rate limit and returns no rate-limit headers
  (`../rate-limits/optum-rate-limits.yml`). Back off on any 429 and on 503/504, which are the two
  most common failures declared across the corpus after 500.
