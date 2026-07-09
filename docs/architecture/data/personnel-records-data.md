# Personnel Records Data

## Purpose

Define document and 201 file data architecture with verification, access logs, retention rules, and document history.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `document_types` | Document type reference. | `id`, `code`, `name`, `document_group`, `is_sensitive`, `requires_verification` | Parent of documents | yes | high |
| `employee_documents` | 201 File Document metadata and employee records. | `id`, `employee_id`, `document_type_id`, `storage_reference`, `document_date`, `status`, `version` | Parents employees, document types | no | high |
| `document_verifications` | Verification events for documents. | `id`, `document_id`, `verified_by`, `verification_status`, `verified_at`, `remarks` | Parent employee documents | no | high |
| `document_access_logs` | Access audit for sensitive documents. | `id`, `document_id`, `user_id`, `access_type`, `accessed_at`, `purpose` | Parents documents, users | no | high |
| `records_retention_rules` | Retention rules by document type or group. | `id`, `document_type_id`, `retention_basis`, `retention_period`, `disposition_action`, `is_active` | Parent document types | yes | high |

## Main Fields

Use document type, owner employee, storage reference, hash/checksum where useful, verification status, version, retention basis, access purpose, and timestamps.

## Relationships

Employee documents belong to employees and document types. Verification and access logs depend on documents. Retention rules depend on document types.

## Indexing Considerations

Index employee ID, document type, status, document date, verification status, retention rule status, and document access timestamps.

## Data Ownership

Owned by records officers and authorized HR users. Storage systems may own binary files; the HRIS owns metadata and access history.

## Data Visibility Rules

201 File Documents are high-sensitivity. Apply least privilege and log access to sensitive document groups.

## Audit Requirements

Audit upload, replacement, verification, rejection, download/view, retention status changes, and deletion/disposition if ever allowed.

## Seeder Requirements

Seed document types and retention rules after manual verification with DepEd and government records management requirements.

## Notes Before Migration Creation

Decide document storage provider, versioning model, checksum strategy, and access log volume retention.
