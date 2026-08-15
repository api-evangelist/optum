---
name: Run a dental pre-care estimate and submit a dental claim
description: Check dental eligibility before treatment, produce a pre-care cost estimate, attach imaging with image intelligence, then submit and track the dental claim through Optum Real for Dental.
api: openapi/optum-real-dental-pre-care-eligibility-api-openapi.yml
operations: [checkEligibility, get_oihub_dental_eligibility_preservice_v1_healthcheck, checkEnhancedEligibility, healthCheckEnhancedDentalEligibility, dentalClaimPrecheck, dentalClaimPrecheckHealth, dntClaimActions, claimStatus, createAttachments, searchAttachments, createAttachmentsImageIntel]
generated: '2026-08-14'
method: generated
---

# Run a dental pre-care estimate and submit a dental claim

Optum Real for Dental is a distinct product line with its own specs and its own token endpoint
(the v3 sentinel endpoint, `/apip/auth/sntl/v1/token`). It is not the medical network with a
different tag.

## 1. Eligibility, before the chair

- `checkEligibility` — `POST /oihub/dental/eligibility/preservice/v1`
  (`openapi/optum-real-dental-pre-care-eligibility-api-openapi.yml`). Pre-service dental
  eligibility.
- `checkEnhancedEligibility` — `POST /oihub/dnt/enh/eligibility/preservice/v1`
  (`openapi/optum-real-dental-pre-care-eligibility-intelligence-api-openapi.yml`). The
  "intelligence" variant with richer benefit detail.
- Health checks: `get_oihub_dental_eligibility_preservice_v1_healthcheck` and
  `healthCheckEnhancedDentalEligibility`.

Two eligibility products exist side by side and the docs do not say which to prefer. Read both
specs and pick on the benefit fields you actually need.

## 2. Pre-care estimate

- `dentalClaimPrecheck` — `POST /claim/precare/v1`
  (`openapi/optum-dental-pre-care-estimate-api-openapi.yml`, base
  `https://apigw.optum.com/oihub/dental`). Returns the estimated patient responsibility for a
  planned treatment before it is performed. This is the operation that makes the whole product
  worth calling: it turns a post-treatment surprise into a pre-treatment conversation.
- `dentalClaimPrecheckHealth` — `GET /claim/precare/v1/healthcheck`.

## 3. Attachments, including imaging

`openapi/optum-real-dental-attachments-api-openapi.yml` (base `.../dental/attachments/v1`):

- `createAttachments` — `POST /attachments/documents`
- `createAttachmentsImageIntel` — `POST /attachments/documents/image-intelligence`. Optum's image
  intelligence pass over dental radiographs.
- `searchAttachments` — `POST /attachments/documents/search`

The older `openapi/optum-dental-attachment-api-openapi.yml` (base `/dentalnetwork/attachments/v1`)
is the Change Healthcare-era surface — Create/Add/Update/Commit/Get/Delete plus
`GetAllParticipatingPayers`, `IsParticipatingPayer` and `GetPayerBusinessRules/me`. **It is the only
API on the entire Optum platform that declares a 429 response**, on all ten of its operations. If
you need documented throttling behaviour, it is here and nowhere else
(`../rate-limits/optum-rate-limits.yml`).

## 4. Submit and track

- `dntClaimActions` — `POST /py/oihub/claim/dnt/submit/v1/graphql`
  (`openapi/optum-real-dental-claim-submission-api-openapi.yml`). Note the path: dental claim
  submission is a **GraphQL** endpoint wrapped in an OpenAPI operation. Introspection is
  auth-gated — an anonymous POST to the gateway returns HTTP 400 `invalid_request` — so the schema
  is not publicly readable. Treat the OpenAPI request body as the contract.
- `claimStatus` — `POST /oihub/dental/claim/inquiry/v1`
  (`openapi/optum-real-dental-claim-status-api-openapi.yml`).

## Cautions

- Consequential writes: submission and attachment operations act on real claims and real PHI.
- No idempotency key anywhere (`../conventions/optum-conventions.yml`). Verify with `claimStatus`
  rather than retrying `dntClaimActions`.
- Check payer participation with `IsParticipatingPayer` / `GetAllParticipatingPayers` before
  attaching — not every dental payer accepts attachments through Optum.
