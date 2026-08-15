---
name: Resolve payers and check connectivity outages
description: Look up the correct Optum payer identifier and its supported capabilities before any transaction, and check live payer outages so a routing failure is not misread as a data error.
api: openapi/optum-payer-list-api-v1-openapi.yml
operations: [getPayers, getPayerListFields, exportPayers, getOutages, getPayerListHealthCheck]
generated: '2026-08-14'
method: generated
---

# Resolve payers and check connectivity outages

Every other Optum transaction depends on naming the payer correctly. This is the lookup step, and
it is the one an integration most often skips and most often regrets.

Auth: OAuth2 client-credentials against `/apip/auth/v2/token`. Base
`https://apigw.optum.com/medicalnetwork/payerlist/v1` (sandbox `https://sandbox-apigw.optum.com/...`).

## Operations

- `getPayers` — `GET /payers`. The payer directory: identifiers plus which transactions each payer
  supports. Match on the payer name and read the identifier; never hard-code a
  `tradingPartnerServiceId` from a sample payload.
- `getPayerListFields` — `GET /fields`. Describes the fields in the payer record, so you can tell
  which capability flags exist before filtering on them.
- `exportPayers` — `GET /payers/export`. Bulk export for caching the directory locally. Prefer this
  over paging `getPayers` on every run — the directory changes slowly.
- `getOutages` — `GET /outages`. **Live payer connectivity outages.** Optum publishes this and
  almost nobody reads it.
- `getPayerListHealthCheck` — `GET /healthcheck`.

## The rule that matters

Check `getOutages` before a batch submission and on any unexplained transaction failure. When a
payer connection is down, eligibility and claim-status calls fail in ways that look like bad input
— wrong member ID, unknown subscriber — and a retry loop will burn through the batch producing the
same wrong diagnosis. An outage is the one failure mode on this platform that is both common and
externally visible in advance.

## Caching

The payer directory is a good local cache; outages are not. Refresh the export daily at most, and
call `getOutages` fresh every time.

## Related

- Eligibility: `../skills/optum-verify-patient-eligibility.md`
- Claims: `../skills/optum-validate-and-submit-a-claim.md`
- Conventions and tracing headers: `../conventions/optum-conventions.yml`
