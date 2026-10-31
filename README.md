# Optum

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Optum, part of UnitedHealth Group, is a health services and technology company that operates one of the largest medical, dental and pharmacy networks in the United States and runs the clearinghouse formerly known as Change Healthcare. Its developer platform (developer.optum.com) publishes eight product lines of RESTful JSON, native X12 EDI and HL7 FHIR R4 APIs: eligibility and coverage discovery, professional and institutional claim validation and submission, claim status, ERA/remittance reports, attachments, payer directory and outage feeds, prior authorization in both X12 278 and FHIR Da Vinci PAS/DTR/CRD form, provider access and bulk member match, dental pre-care estimates and claims, pharmacy formatting and submitter services, payer enrollment and document tracking, and Optum Insight Platform data, code-search and analytics services. Every API is secured with an OAuth2 client-credentials JWT bearer token over TLS 1.2+, with a free canned-response sandbox on a separate host. Optum also publishes an RFC 9727 API catalog at /.well-known/api-catalog, which is how the 59 OpenAPI documents in this repo were harvested.

**Areas:** Company · Healthcare · Health Insurance · Claims · Eligibility · FHIR · Interoperability · Pharmacy · EDI · X12 · Payments · Prior Authorization

## Optum on APIs.io

Everything profiled for Optum is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/optum/](https://apis.io/providers/optum/)** — or go straight to one of the APIs or properties below.

### APIs (163)

- [Optum Real (Medical) API](https://apis.io/apis/optum/optum-real-medical-api/) — Optum Real point-of-care APIs on the oihub gateway: pre-service eligibility, claim pre-check, claim actions, claim inquiry, patient benefit check, document…
- [Optum Interoperability APIs (CMS Patient Access)](https://apis.io/apis/optum/optum-interoperability-apis-cms-patient-access/) — Optum's payer-side CMS Interoperability and Patient Access (CMS-9115-F) surface — Patient Access, Provider Directory and Payer-to-Payer exchange for the…
- [Optum Ambulance Fee Schedule APIs API](https://apis.io/apis/optum/optum-ambulance-fee-schedule-apis-api/) — The Ambulance Fee Schedule APIs API from Optum — 2 operation(s) for ambulance fee schedule apis.
- [Optum Anesthesia Fee APIs API](https://apis.io/apis/optum/optum-anesthesia-fee-apis-api/) — The Anesthesia Fee APIs API from Optum — 1 operation(s) for anesthesia fee apis.
- [Optum APC Calculator APIs API](https://apis.io/apis/optum/optum-apc-calculator-apis-api/) — The APC Calculator APIs API from Optum — 1 operation(s) for apc calculator apis.
- [Optum APC Cross Codes APIs API](https://apis.io/apis/optum/optum-apc-cross-codes-apis-api/) — The APC Cross Codes APIs API from Optum — 3 operation(s) for apc cross codes apis.
- [Optum Application.wadl API](https://apis.io/apis/optum/optum-application-wadl-api/) — The Application.wadl API from Optum — 2 operation(s) for application.wadl.
- [Optum Attachment API](https://apis.io/apis/optum/optum-attachment-api/) — The Attachment API from Optum — 11 operation(s) for attachment.
- [Optum Attachment Document API](https://apis.io/apis/optum/optum-attachment-document-api/) — The Attachment Document API from Optum — 2 operation(s) for attachment document.
- [Optum Attachment Status API](https://apis.io/apis/optum/optum-attachment-status-api/) — The Attachment Status API from Optum — 2 operation(s) for attachment status.
- [Optum Attachment Submission API](https://apis.io/apis/optum/optum-attachment-submission-api/) — Attachment Submission
- [Optum Authentication API](https://apis.io/apis/optum/optum-authentication-api/) — The Authentication API from Optum — 1 operation(s) for authentication.
- [Optum Authorization (Orchestration) API](https://apis.io/apis/optum/optum-authorization-orchestration-api/) — The Authorization (Orchestration) API from Optum — 2 operation(s) for authorization (orchestration).
- [Optum Average Sales Price APIs API](https://apis.io/apis/optum/optum-average-sales-price-apis-api/) — The Average Sales Price APIs API from Optum — 1 operation(s) for average sales price apis.
- [Optum CC/MCC Code and Excludes List for I10CM and I9V1 APIs API](https://apis.io/apis/optum/optum-cc-mcc-code-and-excludes-list-for-i10cm-and-i9v1-apis-api/) — The CC/MCC Code and Excludes List for I10CM and I9V1 APIs API from Optum — 2 operation(s) for cc/mcc code and excludes list for i10cm and i9v1 apis.
- [Optum CCI Edits APIs API](https://apis.io/apis/optum/optum-cci-edits-apis-api/) — The CCI Edits APIs API from Optum — 10 operation(s) for cci edits apis.
- [Optum CCI Edits Code Validator API](https://apis.io/apis/optum/optum-cci-edits-code-validator-api-api/) — The CCI Edits Code Validator API API from Optum — 1 operation(s) for cci edits code validator api.
- [Optum CDI and Coding Support PDF Information API](https://apis.io/apis/optum/optum-cdi-and-coding-support-pdf-information-api/) — The CDI and Coding Support PDF Information API from Optum — 1 operation(s) for cdi and coding support pdf information.
- [Optum CDI Information API](https://apis.io/apis/optum/optum-cdi-information-api/) — The CDI Information API from Optum — 2 operation(s) for cdi information.
- [Optum Check Enhanced Dental Eligibility API](https://apis.io/apis/optum/optum-check-enhanced-dental-eligibility-api/) — The Check Enhanced Dental Eligibility API from Optum — 1 operation(s) for check enhanced dental eligibility.
- [Optum Claim Adjustment Reasons Codes APIs API](https://apis.io/apis/optum/optum-claim-adjustment-reasons-codes-apis-api/) — The Claim Adjustment Reasons Codes APIs API from Optum — 1 operation(s) for claim adjustment reasons codes apis.
- [Optum Claim API](https://apis.io/apis/optum/optum-claim-api/) — The Claim API from Optum — 2 operation(s) for claim.
- [Optum Claim Review API](https://apis.io/apis/optum/optum-claim-review-api/) — The Claim Review API from Optum — 1 operation(s) for claim review.
- [Optum Claim Status API](https://apis.io/apis/optum/optum-claim-status-api-api/) — Claim Status API
- [Optum Claim Status API](https://apis.io/apis/optum/optum-claim-status-api/) — The Claim Status API from Optum — 1 operation(s) for claim status.
- [Optum Claim Status Category Code APIs API](https://apis.io/apis/optum/optum-claim-status-category-code-apis-api/) — The Claim Status Category Code APIs API from Optum — 1 operation(s) for claim status category code apis.
- [Optum Claim Status Code APIs API](https://apis.io/apis/optum/optum-claim-status-code-apis-api/) — The Claim Status Code APIs API from Optum — 1 operation(s) for claim status code apis.
- [Optum Claim Pre Check API](https://apis.io/apis/optum/optum-claimprecheck-api/) — The ClaimPreCheck API from Optum — 1 operation(s) for claimprecheck.
- [Optum Clinical Diagnostic Laboratory APIs API](https://apis.io/apis/optum/optum-clinical-diagnostic-laboratory-apis-api/) — The Clinical Diagnostic Laboratory APIs API from Optum — 1 operation(s) for clinical diagnostic laboratory apis.
- [Optum CMS HCC APIs API](https://apis.io/apis/optum/optum-cms-hcc-apis-api/) — The CMS HCC APIs API from Optum — 3 operation(s) for cms hcc apis.
- [Optum CMS IOM's Policy APIs API](https://apis.io/apis/optum/optum-cms-iom-s-policy-apis-api/) — The CMS IOM's Policy APIs API from Optum — 1 operation(s) for cms iom's policy apis.
- [Optum CMS Transmittal APIs API](https://apis.io/apis/optum/optum-cms-transmittal-apis-api/) — The CMS Transmittal APIs API from Optum — 3 operation(s) for cms transmittal apis.
- [Optum Code Book APIs API](https://apis.io/apis/optum/optum-code-book-apis-api/) — The Code Book APIs API from Optum — 2 operation(s) for code book apis.
- [Optum Code Fee API](https://apis.io/apis/optum/optum-code-fee-api/) — The Code Fee API from Optum — 4 operation(s) for code fee.
- [Optum Code History APIs API](https://apis.io/apis/optum/optum-code-history-apis-api/) — The Code History APIs API from Optum — 1 operation(s) for code history apis.
- [Optum Code Image APIs API](https://apis.io/apis/optum/optum-code-image-apis-api/) — The Code Image APIs API from Optum — 3 operation(s) for code image apis.
- [Optum Code Information API](https://apis.io/apis/optum/optum-code-information-api/) — The Code Information API from Optum — 15 operation(s) for code information.
- [Optum Code Information APIs API](https://apis.io/apis/optum/optum-code-information-apis-api/) — The Code Information APIs API from Optum — 9 operation(s) for code information apis.
- [Optum Code Specific Guidelines API](https://apis.io/apis/optum/optum-code-specific-guidelines-api/) — The Code Specific Guidelines API from Optum — 2 operation(s) for code specific guidelines.
- [Optum Code Specific Guidelines APIs API](https://apis.io/apis/optum/optum-code-specific-guidelines-apis-api/) — The Code Specific Guidelines APIs API from Optum — 2 operation(s) for code specific guidelines apis.
- [Optum Coding Documentation Guideline APIs API](https://apis.io/apis/optum/optum-coding-documentation-guideline-apis-api/) — The Coding Documentation Guideline APIs API from Optum — 2 operation(s) for coding documentation guideline apis.
- [Optum Coding Support API](https://apis.io/apis/optum/optum-coding-support-api/) — The Coding Support API from Optum — 1 operation(s) for coding support.
- [Optum Coding Tips API](https://apis.io/apis/optum/optum-coding-tips-api-api/) — The Coding Tips API API from Optum — 2 operation(s) for coding tips api.
- [Optum Color Codes API](https://apis.io/apis/optum/optum-color-codes-api/) — The Color Codes API from Optum — 5 operation(s) for color codes.
- [Optum Color codes APIs API](https://apis.io/apis/optum/optum-color-codes-apis-api/) — The Color codes APIs API from Optum — 23 operation(s) for color codes apis.
- [Optum Compliance APIs API](https://apis.io/apis/optum/optum-compliance-apis-api/) — The Compliance APIs API from Optum — 5 operation(s) for compliance apis.
- [Optum Consumer Code Manager API](https://apis.io/apis/optum/optum-consumer-code-manager-api-api/) — The Consumer Code Manager API API from Optum — 1 operation(s) for consumer code manager api.
- [Optum Coverage Discovery API](https://apis.io/apis/optum/optum-coverage-discovery-api/) — Create and retrieve asynchronous Coverage Discovery tasks. Coverage Discovery paths and add-ons are enabled per customer and are not included automatically.…
- [Optum Create Attachments API](https://apis.io/apis/optum/optum-create-attachments-api/) — Operations for creating and uploading attachments.
- [Optum Cross Coder API](https://apis.io/apis/optum/optum-cross-coder-api-api/) — The Cross Coder API API from Optum — 3 operation(s) for cross coder api.
- [Optum Data File API](https://apis.io/apis/optum/optum-data-file-api/) — The Data File API from Optum — 2 operation(s) for data file.
- [Optum Decision Support Record Service API](https://apis.io/apis/optum/optum-decisionsupportrecordservice-api/) — The DecisionSupportRecordService API from Optum — 2 operation(s) for decisionsupportrecordservice.
- [Optum Dental Claim Actions API](https://apis.io/apis/optum/optum-dental-claim-actions-api/) — The Dental Claim Actions API from Optum — 1 operation(s) for dental claim actions.
- [Optum Determination API](https://apis.io/apis/optum/optum-determination-api/) — The Determination API from Optum — 2 operation(s) for determination.
- [Optum Device Codes APIs API](https://apis.io/apis/optum/optum-device-codes-apis-api/) — The Device Codes APIs API from Optum — 3 operation(s) for device codes apis.
- [Optum Device Offset Codes Pair APIs API](https://apis.io/apis/optum/optum-device-offset-codes-pair-apis-api/) — The Device Offset Codes Pair APIs API from Optum — 1 operation(s) for device offset codes pair apis.
- [Optum Diagnostic Related Groups (DRG) Indicators APIs API](https://apis.io/apis/optum/optum-diagnostic-related-groups-drg-indicators-apis-api/) — The Diagnostic Related Groups (DRG) Indicators APIs API from Optum — 1 operation(s) for diagnostic related groups (drg) indicators apis.
- [Optum Discovery API](https://apis.io/apis/optum/optum-discovery-api/) — The Discovery API from Optum — 1 operation(s) for discovery.
- [Optum DME and PEN Fee Schedule APIs API](https://apis.io/apis/optum/optum-dme-and-pen-fee-schedule-apis-api/) — The DME and PEN Fee Schedule APIs API from Optum — 3 operation(s) for dme and pen fee schedule apis.
- [Optum Document Retrieve API](https://apis.io/apis/optum/optum-documentretrieve-api/) — The documentRetrieve API from Optum — 1 operation(s) for documentretrieve.
- [Optum DRG Calculator APIs API](https://apis.io/apis/optum/optum-drg-calculator-apis-api/) — The DRG Calculator APIs API from Optum — 1 operation(s) for drg calculator apis.
- [Optum DRG Codes API](https://apis.io/apis/optum/optum-drg-codes-api/) — The DRG Codes API from Optum — 1 operation(s) for drg codes.
- [Optum DRG Information APIs API](https://apis.io/apis/optum/optum-drg-information-apis-api/) — The DRG Information APIs API from Optum — 6 operation(s) for drg information apis.
- [Optum Dtr Capability Statement API](https://apis.io/apis/optum/optum-dtrcapabilitystatement-api/) — The DtrCapabilityStatement API from Optum — 1 operation(s) for dtrcapabilitystatement.
- [Optum Eligibility API](https://apis.io/apis/optum/optum-eligibility-api/) — Medical Eligibility
- [Optum Eligibility Requests API](https://apis.io/apis/optum/optum-eligibility-requests-api/) — Submit new real-time eligibility transactions. These endpoints accept either a normalized JSON request or a JSON request body with `x12` set to the X12 270…
- [Optum Eligibility Transactions API](https://apis.io/apis/optum/optum-eligibility-transactions-api/) — Retrieve previously processed real-time eligibility transactions. Use these endpoints to list transactions, filter by status, date range, patient details,…
- [Optum ERA Enrollment API](https://apis.io/apis/optum/optum-era-enrollment-api-api/) — ERA Enrollment API
- [Optum Exports API](https://apis.io/apis/optum/optum-exports-api/) — The Exports API from Optum — 1 operation(s) for exports.
- [Optum Facility Compliance APIs API](https://apis.io/apis/optum/optum-facility-compliance-apis-api/) — The Facility Compliance APIs API from Optum — 12 operation(s) for facility compliance apis.
- [Optum Federal Register Addendum B API](https://apis.io/apis/optum/optum-federal-register-addendum-b-api-api/) — The Federal Register Addendum B API API from Optum — 1 operation(s) for federal register addendum b api.
- [Optum Federal Register Addendum B History API](https://apis.io/apis/optum/optum-federal-register-addendum-b-history-api-api/) — The Federal Register Addendum B History API API from Optum — 1 operation(s) for federal register addendum b history api.
- [Optum Fields API](https://apis.io/apis/optum/optum-fields-api/) — The Fields API from Optum — 1 operation(s) for fields.
- [Optum Filter Dictionary Terms API](https://apis.io/apis/optum/optum-filter-dictionary-terms-api/) — Filter dictionary terms from a given string
- [Optum Future Codes APIs API](https://apis.io/apis/optum/optum-future-codes-apis-api/) — The Future Codes APIs API from Optum — 1 operation(s) for future codes apis.
- [Optum Get Doc Counts API](https://apis.io/apis/optum/optum-getdoccounts-api/) — The GetDocCounts API from Optum — 1 operation(s) for getdoccounts.
- [Optum Get Document Status API](https://apis.io/apis/optum/optum-getdocumentstatus-api/) — The GetDocumentStatus API from Optum — 1 operation(s) for getdocumentstatus.
- [Optum Get File Status API](https://apis.io/apis/optum/optum-getfilestatus-api/) — The GetFileStatus API from Optum — 1 operation(s) for getfilestatus.
- [Optum Get Listof Doc Status API](https://apis.io/apis/optum/optum-getlistofdocstatus-api/) — The GetListofDocStatus API from Optum — 1 operation(s) for getlistofdocstatus.
- [Optum Get List Of File Status API](https://apis.io/apis/optum/optum-getlistoffilestatus-api/) — The GetListOfFileStatus API from Optum — 1 operation(s) for getlistoffilestatus.
- [Optum HCC Information API](https://apis.io/apis/optum/optum-hcc-information-api/) — The HCC Information API from Optum — 4 operation(s) for hcc information.
- [Optum HCPCS Table of Drugs API](https://apis.io/apis/optum/optum-hcpcs-table-of-drugs-api-api/) — The HCPCS Table of Drugs API API from Optum — 1 operation(s) for hcpcs table of drugs api.
- [Optum Health Care Decision Reason API](https://apis.io/apis/optum/optum-health-care-decision-reason-api-api/) — The Health Care Decision Reason API API from Optum — 1 operation(s) for health care decision reason api.
- [Optum Health Check API](https://apis.io/apis/optum/optum-health-check-api/) — The Health Check API from Optum — 7 operation(s) for health check.
- [Optum I-OCE Edits APIs API](https://apis.io/apis/optum/optum-i-oce-edits-apis-api/) — The I-OCE Edits APIs API from Optum — 4 operation(s) for i-oce edits apis.
- [Optum I10PCS Code Builder APIs API](https://apis.io/apis/optum/optum-i10pcs-code-builder-apis-api/) — The I10PCS Code Builder APIs API from Optum — 3 operation(s) for i10pcs code builder apis.
- [Optum ICD10 Mapping API](https://apis.io/apis/optum/optum-icd10-mapping-api/) — The ICD10 Mapping API from Optum — 1 operation(s) for icd10 mapping.
- [Optum ICD9 Mapping API](https://apis.io/apis/optum/optum-icd9-mapping-api/) — The ICD9 Mapping API from Optum — 1 operation(s) for icd9 mapping.
- [Optum Image Intelligence API](https://apis.io/apis/optum/optum-image-intelligence-api/) — Operations for enabling Image Intelligence for attachments.
- [Optum Inquiry API](https://apis.io/apis/optum/optum-inquiry-api/) — The Inquiry API from Optum — 3 operation(s) for inquiry.
- [Optum Institutional Claims API](https://apis.io/apis/optum/optum-institutional-claims-api/) — Institutional Claims
- [Optum LCD API](https://apis.io/apis/optum/optum-lcd-api/) — The LCD API from Optum — 4 operation(s) for lcd.
- [Optum Mapping APIs API](https://apis.io/apis/optum/optum-mapping-apis-api/) — The Mapping APIs API from Optum — 4 operation(s) for mapping apis.
- [Optum MCE Associated ICD10 APIs API](https://apis.io/apis/optum/optum-mce-associated-icd10-apis-api/) — The MCE Associated ICD10 APIs API from Optum — 3 operation(s) for mce associated icd10 apis.
- [Optum MCE Associated ICD9 APIs API](https://apis.io/apis/optum/optum-mce-associated-icd9-apis-api/) — The MCE Associated ICD9 APIs API from Optum — 1 operation(s) for mce associated icd9 apis.
- [Optum MCE Edits ICD9 and ICD10 API](https://apis.io/apis/optum/optum-mce-edits-icd9-and-icd10-api-api/) — The MCE Edits ICD9 and ICD10 API API from Optum — 3 operation(s) for mce edits icd9 and icd10 api.
- [Optum MDC Optimizing Tips APIs API](https://apis.io/apis/optum/optum-mdc-optimizing-tips-apis-api/) — The MDC Optimizing Tips APIs API from Optum — 2 operation(s) for mdc optimizing tips apis.
- [Optum Medically Unlikely Edits(MUEs) APIs API](https://apis.io/apis/optum/optum-medically-unlikely-edits-mues-apis-api/) — The Medically Unlikely Edits(MUEs) APIs API from Optum — 1 operation(s) for medically unlikely edits(mues) apis.
- [Optum Medicare Carrier Localities API](https://apis.io/apis/optum/optum-medicare-carrier-localities-api/) — The Medicare Carrier Localities API from Optum — 1 operation(s) for medicare carrier localities.
- [Optum Medicare Coverage Policy for part A and Part B APIs API](https://apis.io/apis/optum/optum-medicare-coverage-policy-for-part-a-and-part-b-apis-api/) — The Medicare Coverage Policy for part A and Part B APIs API from Optum — 4 operation(s) for medicare coverage policy for part a and part b apis.
- [Optum Medicare Fee Schedule APIs API](https://apis.io/apis/optum/optum-medicare-fee-schedule-apis-api/) — The Medicare Fee Schedule APIs API from Optum — 10 operation(s) for medicare fee schedule apis.
- [Optum Medicare Policy API](https://apis.io/apis/optum/optum-medicare-policy-api/) — The Medicare Policy API from Optum — 3 operation(s) for medicare policy.
- [Optum Merck Manual API](https://apis.io/apis/optum/optum-merck-manual-api-api/) — The Merck Manual API API from Optum — 2 operation(s) for merck manual api.
- [Optum Modifier CrossWalk API](https://apis.io/apis/optum/optum-modifier-crosswalk-api-api/) — The Modifier CrossWalk API API from Optum — 2 operation(s) for modifier crosswalk api.
- [Optum Modifiers API](https://apis.io/apis/optum/optum-modifiers-api/) — The Modifiers API from Optum — 5 operation(s) for modifiers.
- [Optum Modifiers APIs API](https://apis.io/apis/optum/optum-modifiers-apis-api/) — The Modifiers APIs API from Optum — 6 operation(s) for modifiers apis.
- [Optum MPFS National Payment Table Facility APIs API](https://apis.io/apis/optum/optum-mpfs-national-payment-table-facility-apis-api/) — The MPFS National Payment Table Facility APIs API from Optum — 1 operation(s) for mpfs national payment table facility apis.
- [Optum National Charge Data API](https://apis.io/apis/optum/optum-national-charge-data-api-api/) — The National Charge Data API API from Optum — 1 operation(s) for national charge data api.
- [Optum National Drug Code API](https://apis.io/apis/optum/optum-national-drug-code-api-api/) — The National Drug Code API API from Optum — 1 operation(s) for national drug code api.
- [Optum Next Question API](https://apis.io/apis/optum/optum-nextquestion-api/) — The NextQuestion API from Optum — 1 operation(s) for nextquestion.
- [Optum Noa API](https://apis.io/apis/optum/optum-noa-api/) — The Noa API from Optum — 2 operation(s) for noa.
- [Optum Not Otherwise Classified (NOC) Drug Pricing APIs API](https://apis.io/apis/optum/optum-not-otherwise-classified-noc-drug-pricing-apis-api/) — The Not Otherwise Classified (NOC) Drug Pricing APIs API from Optum — 1 operation(s) for not otherwise classified (noc) drug pricing apis.
- [Optum Notes Information APIs API](https://apis.io/apis/optum/optum-notes-information-apis-api/) — The Notes Information APIs API from Optum — 6 operation(s) for notes information apis.
- [Optum Oihub API](https://apis.io/apis/optum/optum-oihub-api/) — The Oihub API from Optum — 1 operation(s) for oihub.
- [Optum Operation Definition API](https://apis.io/apis/optum/optum-operationdefinition-api/) — The OperationDefinition API from Optum — 1 operation(s) for operationdefinition.
- [Optum Opps Cross Codes API](https://apis.io/apis/optum/optum-opps-cross-codes-api-api/) — The Opps Cross Codes API API from Optum — 1 operation(s) for opps cross codes api.
- [Optum OPPS CrossCode Code API](https://apis.io/apis/optum/optum-opps-crosscode-code-api/) — The OPPS CrossCode Code API from Optum — 1 operation(s) for opps crosscode code.
- [Optum OPSI Codes APIs API](https://apis.io/apis/optum/optum-opsi-codes-apis-api/) — The OPSI Codes APIs API from Optum — 3 operation(s) for opsi codes apis.
- [Optum Specialty Articles API](https://apis.io/apis/optum/optum-optum-specialty-articles-api/) — The Optum Specialty Articles API from Optum — 1 operation(s) for optum specialty articles.
- [Optum Order Management API](https://apis.io/apis/optum/optum-order-management-api/) — The Order Management API from Optum — 10 operation(s) for order management.
- [Optum Order Sign API](https://apis.io/apis/optum/optum-ordersign-api/) — The OrderSign API from Optum — 1 operation(s) for ordersign.
- [Optum Outages API](https://apis.io/apis/optum/optum-outages-api/) — The Outages API from Optum — 1 operation(s) for outages.
- [Optum Pas Capability Statement API](https://apis.io/apis/optum/optum-pascapabilitystatement-api/) — The PasCapabilityStatement API from Optum — 1 operation(s) for pascapabilitystatement.
- [Optum Payers API](https://apis.io/apis/optum/optum-payers-api/) — The Payers API from Optum — 1 operation(s) for payers.
- [Optum Payersheet API](https://apis.io/apis/optum/optum-payersheet-api/) — API to process Payersheet information
- [Optum Payments API](https://apis.io/apis/optum/optum-payments-api/) — The Payments API from Optum — 2 operation(s) for payments.
- [Optum Policy Lookup APIs API](https://apis.io/apis/optum/optum-policy-lookup-apis-api/) — The Policy Lookup APIs API from Optum — 4 operation(s) for policy lookup apis.
- [Optum Prepaydme API](https://apis.io/apis/optum/optum-prepaydme-api/) — The prepaydme API from Optum — 1 operation(s) for prepaydme.
- [Optum Prepaylab API](https://apis.io/apis/optum/optum-prepaylab-api/) — The prepaylab API from Optum — 1 operation(s) for prepaylab.
- [Optum Print Code Detail Summary API](https://apis.io/apis/optum/optum-print-code-detail-summary-api-api/) — The Print Code Detail Summary API API from Optum — 1 operation(s) for print code detail summary api.
- [Optum prior auth API](https://apis.io/apis/optum/optum-prior-auth-api-api/) — The prior auth api API from Optum — 1 operation(s) for prior auth api.
- [Optum Professional Claims API](https://apis.io/apis/optum/optum-professional-claims-api/) — Professional Claims
- [Optum Prometheus API](https://apis.io/apis/optum/optum-prometheus-api/) — The Prometheus API from Optum — 2 operation(s) for prometheus.
- [Optum Provider Lookup APIs API](https://apis.io/apis/optum/optum-provider-lookup-apis-api/) — The Provider Lookup APIs API from Optum — 1 operation(s) for provider lookup apis.
- [Optum Provider Participation List API](https://apis.io/apis/optum/optum-provider-participation-list-api/) — The Provider Participation List API from Optum — 1 operation(s) for provider participation list.
- [Optum Provider Access Bulk Member Match API](https://apis.io/apis/optum/optum-provideraccessbulkmembermatch-api/) — The ProviderAccessBulkMemberMatch API from Optum — 1 operation(s) for provideraccessbulkmembermatch.
- [Optum Provider Access Bulk Member Match Status API](https://apis.io/apis/optum/optum-provideraccessbulkmembermatchstatus-api/) — The ProviderAccessBulkMemberMatchStatus API from Optum — 1 operation(s) for provideraccessbulkmembermatchstatus.
- [Optum Provider Access Da Vinci Export API](https://apis.io/apis/optum/optum-provideraccessdavinciexport-api/) — The ProviderAccessDaVinciExport API from Optum — 1 operation(s) for provideraccessdavinciexport.
- [Optum Provider Access Da Vinci Export Download API](https://apis.io/apis/optum/optum-provideraccessdavinciexportdownload-api/) — The ProviderAccessDaVinciExportDownload API from Optum — 1 operation(s) for provideraccessdavinciexportdownload.
- [Optum QPP MIPS APIs API](https://apis.io/apis/optum/optum-qpp-mips-apis-api/) — The QPP MIPS APIs API from Optum — 4 operation(s) for qpp mips apis.
- [Optum Questionnaire Package API](https://apis.io/apis/optum/optum-questionnairepackage-api/) — The QuestionnairePackage API from Optum — 1 operation(s) for questionnairepackage.
- [Optum Reference Code API](https://apis.io/apis/optum/optum-reference-code-api/) — The Reference Code API from Optum — 6 operation(s) for reference code.
- [Optum Release Dates API](https://apis.io/apis/optum/optum-release-dates-api-api/) — The Release Dates API API from Optum — 1 operation(s) for release dates api.
- [Optum Remittance Advice Remark Codes APIs API](https://apis.io/apis/optum/optum-remittance-advice-remark-codes-apis-api/) — The Remittance Advice Remark Codes APIs API from Optum — 1 operation(s) for remittance advice remark codes apis.
- [Optum Report API](https://apis.io/apis/optum/optum-report-api/) — The Report API from Optum — 3 operation(s) for report.
- [Optum Reports API](https://apis.io/apis/optum/optum-reports-api/) — The Reports API from Optum — 1 operation(s) for reports.
- [Optum Revenue Code API](https://apis.io/apis/optum/optum-revenue-code-api/) — The Revenue Code API from Optum — 4 operation(s) for revenue code.
- [Optum Revenue Codes API](https://apis.io/apis/optum/optum-revenue-codes-api-api/) — The Revenue Codes API API from Optum — 4 operation(s) for revenue codes api.
- [Optum Review Attachments API](https://apis.io/apis/optum/optum-review-attachments-api/) — Operations for retrieving attachments for review.
- [Optum Roster Management API](https://apis.io/apis/optum/optum-roster-management-api/) — The Roster Management API from Optum — 1 operation(s) for roster management.
- [Optum State List Fee Schedule APIs API](https://apis.io/apis/optum/optum-state-list-fee-schedule-apis-api/) — The State List Fee Schedule APIs API from Optum — 1 operation(s) for state list fee schedule apis.
- [Optum Submission API](https://apis.io/apis/optum/optum-submission-api/) — The Submission API from Optum — 2 operation(s) for submission.
- [Optum Submit API](https://apis.io/apis/optum/optum-submit-api/) — The Submit API from Optum — 1 operation(s) for submit.
- [Optum Submit Attachment API](https://apis.io/apis/optum/optum-submitattachment-api/) — The SubmitAttachment API from Optum — 1 operation(s) for submitattachment.
- [Optum Submitter API Request HTTP Controller API](https://apis.io/apis/optum/optum-submitter-api-request-http-controller-api/) — The submitter-api-request-http-controller API from Optum — 1 operation(s) for submitter-api-request-http-controller.
- [Optum Supporting Documentation APIs API](https://apis.io/apis/optum/optum-supporting-documentation-apis-api/) — The Supporting Documentation APIs API from Optum — 2 operation(s) for supporting documentation apis.
- [Optum Telecom Format API](https://apis.io/apis/optum/optum-telecom-format-api/) — API to format details received in a request
- [Optum Type of Bill I/OCE Edit OPPS API](https://apis.io/apis/optum/optum-type-of-bill-i-oce-edit-opps-api/) — The Type of Bill I/OCE Edit OPPS API from Optum — 2 operation(s) for type of bill i/oce edit opps.
- [Optum UB04 Code Lists API](https://apis.io/apis/optum/optum-ub04-code-lists-api/) — The UB04 Code Lists API from Optum — 1 operation(s) for ub04 code lists.
- [Optum V3 Ingestion API](https://apis.io/apis/optum/optum-v3-ingestion-api/) — ODX V3 Ingestion Service API for processing XDR Request in P&R request with HL7 V3 payload
- [Optum Wage Index API](https://apis.io/apis/optum/optum-wage-index-api-api/) — The Wage Index API API from Optum — 1 operation(s) for wage index api.
- [Optum Document Reference API](https://apis.io/apis/optum/optum-document-reference-api/) — The Document Reference API from Optum — 1 operation(s) for document reference.
- [Optum Query Service API](https://apis.io/apis/optum/optum-query-service-api/) — The Query Service API from Optum — 1 operation(s) for query service.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Optum Webhooks](https://apis.io/asyncapis/optum/optum-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [optum](https://apis.io/servers/optum/optum/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Optum Agentic Access](https://apis.io/agentic-access/optum/optum-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Optum Servers And Provenance Overlay](https://apis.io/overlays/optum/optum-servers-and-provenance-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Optum Authentication](https://apis.io/security/optum/optum-authentication/)
- [Optum Domain Security](https://apis.io/security/optum/optum-domain-security/)
- [Optum Vulnerability Disclosure](https://apis.io/security/optum/optum-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Optum Scopes](https://apis.io/scopes/optum/optum-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Optum Plans Pricing](https://apis.io/plans/optum/optum-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Optum Rate Limits](https://apis.io/rate-limits/optum/optum-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.optum.com/)
- [Documentation](https://developer.optum.com/apitools/docs/getting-started)
- [Getting started](https://developer.optum.com/eligibilityandclaims/docs/get-started-with-optum-api)
- [API reference](https://developer.optum.com/eligibilityandclaims/reference/api-overview)
- [Pricing](https://marketplace.optum.com/apiservices/api-sandbox-access)
- [Sign up](https://marketplace.optum.com/apiservices/api-sandbox-access)
- [Support](https://community.optum.com/developers/home)
- [Blog](https://www.optum.com/en/newsroom.html)
- [Security](https://www.optum.com/vulnerability.html)
- [Compliance](https://business.optum.com/en/federal-government/about-optum-serve/certifications-partnerships.html)
- [Terms of service](https://www.optum.com/terms-of-use.html)
- [Privacy policy](https://www.optum.com/privacy-policy.html)
- [GitHub](https://github.com/Optum)
- [Status](https://status.optum.com/)

## API Evangelist rating

**Kin Score 57.0** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 89.3 |
| Contract quality | 60.2 |
| Contract governance | 18.2 |
| Operational transparency | 44.7 |
| Developer ergonomics | 45.8 |
| Access clarity | 52.6 |

**Agent readiness 37.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 52.3** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/optum/](https://apis.io/providers/optum/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Optum: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/optum/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
