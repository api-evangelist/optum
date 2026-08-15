---
name: Run a FHIR Da Vinci prior authorization
description: Discover coverage requirements with CDS Hooks, gather the DTR questionnaire, then submit and inquire on a prior authorization through Optum Real's FHIR R4 Da Vinci PAS implementation.
api: openapi/optum-real-prior-authorization-api-openapi.yml
operations: [getDiscovery, orderSign, getPasCapabilityStatement, getDtrCapabilityStatement, getOperationDefinition, getQuestionnairePackage, getNextQuestion, submitClaim, inquireClaim, submitAttachment, getDocumentReference, healthCheck]
generated: '2026-08-14'
method: generated
---

# Run a FHIR Da Vinci prior authorization

Optum Real implements the HL7 Da Vinci prior-authorization stack — CRD (CDS Hooks), DTR
(questionnaires) and PAS (submit/inquire) — as one FHIR R4 API. Every path is parameterised by
`{payerId}` and `{lob}` (line of business), so the same operation targets different payers.

Auth is the **v3 / sentinel** token endpoint: `POST https://apigw.optum.com/apip/auth/sntl/v1/token`
(sandbox: `https://sandbox-apigw.optum.com/...`). See `../authentication/optum-authentication.yml`.

## 1. Learn what this payer supports

- `getPasCapabilityStatement` — `GET .../fhirpa/R4/{payerId}/{lob}/pas/metadata`
- `getDtrCapabilityStatement` — `GET .../fhirpa/R4/{payerId}/{lob}/dtr/metadata`
- `getOperationDefinition` — `GET .../fhirpa/R4/{payerId}/{lob}/operation-definition/{operation}`

Read the CapabilityStatement before assuming an operation exists for a given payer/LOB pair. This
is the one place on the Optum platform where per-tenant capability is genuinely machine-readable.

## 2. Coverage Requirements Discovery (CRD)

- `getDiscovery` — `GET .../cdsHooksServer/{payerId}/{lob}/api/cds-services` lists the CDS Hooks
  services this payer exposes.
- `orderSign` — `POST .../cdsHooksServer/{payerId}/{lob}/api/cds-services/crd-order-sign` fires the
  order-sign hook and returns whether prior authorization is required at all. Run this first: the
  cheapest prior authorization is the one you learn you do not need.

## 3. Documentation Templates and Rules (DTR)

- `getQuestionnairePackage` — `POST .../Questionnaire/$questionnaire-package` returns the
  questionnaire and the CQL-driven population logic for this order.
- `getNextQuestion` — `POST .../Questionnaire/$next-question` drives adaptive forms one question at
  a time. Use it rather than rendering the whole questionnaire when the payer supports it.

## 4. Submit and follow up

- `submitClaim` — `POST .../Claim/$submit`. **This is the request.** Consequential; gate it behind
  a human.
- `submitAttachment` — `POST .../Claim/$submit-attachment` attaches supporting clinical
  documentation.
- `getDocumentReference` — `GET .../document-reference` retrieves referenced documents.
- `inquireClaim` — `POST .../Claim/$inquire` checks status. There is **no webhook** for prior
  authorization — polling `$inquire` is the only status mechanism.
- `healthCheck` — `GET /oihub/fhirpriorauth/v1/health-check`.

## Cautions

- These are FHIR operations, not the JSON transaction shape used by the Medical Network APIs. The
  request bodies are FHIR Bundles; validate against the profiles in the CapabilityStatement.
- There is a **second, non-FHIR** prior-authorization surface —
  `openapi/optum-prior-authorization-v1-openapi.yml` (X12 278 submission/inquiry/determination/NOA
  with `/x12` siblings). Pick one deliberately: they are different products, not versions of each
  other.
- No idempotency key exists. A retried `$submit` may create a duplicate authorization request.
- PHI throughout. Sandbox is canned-response only and forbids real patient data.
