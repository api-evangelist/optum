---
name: Validate and submit a professional or institutional claim
description: Run an X12 837P/837I claim through Optum's validation endpoint before submitting it, submit it, then reconcile the 277CA acknowledgement and 835 remittance from the reports API.
api: openapi/optum-medical-network-professional-claims-v3-openapi.yml
operations: [validateClaim, processClaim, rawX12Validation, rawX12Submission, healthCheck, validateRawX12, processClaim_1, claimstatus, list_reports_v2_reports_get, get_single_report_v2_reports__filename__get, convert_report_277_v2_reports__filename__277_get, convert_report_835_v2_reports__filename__835_get, delete_single_report_v2_reports__filename__delete]
generated: '2026-08-14'
method: generated
---

# Validate and submit a professional or institutional claim

This is the highest-consequence flow on the Optum platform. A submitted claim is a real financial
transaction against a payer. `../agentic-access/optum-agentic-access.yml` classifies it `acting`;
require human confirmation before `processClaim`.

## Choose the right spec

- **Professional (837P)** — `openapi/optum-medical-network-professional-claims-v3-openapi.yml`
- **Institutional (837I)** — `openapi/optum-medical-network-institutional-claims-v1-openapi.yml`

Both expose the same four-operation shape plus a health check.

## Always validate first

- `validateClaim` — `POST .../validation`. Runs Optum's edits without submitting. This step is free
  of consequence and is the entire reason to use a clearinghouse; skipping it converts a fixable
  syntax problem into a payer rejection weeks later.
- `rawX12Validation` (professional) / `validateRawX12` (institutional) — same check for a claim you
  already hold as X12.

Only when validation is clean:

- `processClaim` — `POST .../submission`. **Irreversible.** Submits the claim.
- `rawX12Submission` (professional) / `processClaim_1` (institutional) — native X12 submission.

## Retry rule — read this before writing any retry logic

Optum documents **no idempotency key** on any endpoint
(`../conventions/optum-conventions.yml`). If `processClaim` times out you do not know whether the
claim landed. Do **not** blind-retry. Instead:

1. Call `claimstatus` (`openapi/optum-medical-network-claim-status-v2-openapi.yml`,
   `POST /medicalnetwork/claimstatus/v2/`) with the claim's `controlNumber` and payer identifiers.
2. Or look for the claim in the acknowledgement reports below.

Server-side de-duplication happens on payer/claim identifiers, but that is a business rule, not a
contract you can rely on for exactly-once submission.

## Reconcile the results

The reports API (`openapi/optum-medical-network-claims-responses-and-reports-v2-openapi.yml`) is a
pull, not a push — there is no event feed:

- `list_reports_v2_reports_get` — `GET /` lists available report files.
- `convert_report_277_v2_reports__filename__277_get` — renders the 277CA claim acknowledgement as
  JSON. **This is where you learn whether the claim was actually accepted**, not from the HTTP
  status on submission.
- `convert_report_835_v2_reports__filename__835_get` — renders the 835 electronic remittance advice
  as JSON: what was paid, adjusted and denied.
- `get_single_report_v2_reports__filename__get` — downloads the raw file. Large files may return
  413; the API supports streaming for these (added in the May 2021 v2 release).
- `delete_single_report_v2_reports__filename__delete` — removes a report once processed. Destructive;
  only after you have persisted the content.

## Attachments

If the payer requires documentation, use
`openapi/optum-medical-network-attachments-submission-v1-openapi.yml#upload`
(`POST /uploads`) and poll `GET /{traceId}` on the attachment status API. Attachments carry PHI —
never route them through a sandbox host.
