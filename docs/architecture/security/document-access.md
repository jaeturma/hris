# Document Access

Document access must be explicit, purpose-bound, and logged for sensitive records.

## Document Categories

| Category | Examples | Default sensitivity | Access model |
| --- | --- | --- | --- |
| Applicant documents | Application requirements, eligibility, credentials | high | Applicant own view plus assigned HR/HRMPSB/evaluators |
| Employee 201 File Documents | Appointment papers, service records, credentials, official personnel documents | high | Records/HR roles, employee own view where allowed |
| Restricted documents | Performance ratings, disciplinary/confidential records, medical or highly sensitive documents | high | Explicit restricted permission only |
| HRMPSB records | Evaluation sheets, interview notes, rankings, recommendations | high | Assigned cycle members and authorized HR/auditors |
| Competency records | Assessments, gap analyses, IDPs, readiness evidence | high | HR, supervisor/evaluator, employee own view where allowed |
| Reports and exports | CAR, RQA-style outputs, audit reports, payroll exports | high | Permission-gated and export-logged |

## Required Permissions

- `employee-documents.view`
- `employee-documents.view-restricted`
- `employee-documents.upload`
- `employee-documents.verify`
- `document-access-logs.view`
- `reports.export`

## Access Logging

Log the following:

- View restricted document.
- Download/export document.
- Upload or replace document.
- Verify, reject, or return document.
- Change document type sensitivity.
- Change retention rule.

## Rules

- Do not expose storage paths directly.
- Never rely on frontend hiding for document security.
- Use generated filenames and safe storage references.
- Restrict previews and downloads separately when needed.
- Employee and applicant self-service must be limited to own documents.
- HRMPSB/evaluator document access must be limited to assigned cycles/applications.

## Notes Before Implementation

Decide storage provider, document classification, preview/download rules, checksum strategy, and retention rules before building document modules.
