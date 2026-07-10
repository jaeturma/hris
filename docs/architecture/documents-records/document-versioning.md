# Document Versioning

## Purpose

Define versioning for uploaded evidence, corrected submissions, updated credentials, generated reports, appointment documents, policy issuances, templates, and signed documents.

## Recommended Metadata

`document_id`, `version_number`, `previous_version_id`, `supersedes_version_id`, `original_filename`, `stored_filename`, `file_hash`, `mime_type`, `file_size`, `uploaded_by`, `uploaded_at`, `source`, `reason_for_new_version`, `verified_by`, `verified_at`, `finalized_at`, `signed_at`, `archived_at`.

## Versioning Rules

- Do not overwrite a prior version.
- Signed documents cannot be replaced in place.
- A corrected signed document must become a new official version.
- Supersession must preserve the earlier document.
- Draft templates and final documents must remain distinct.
- Duplicate-file detection must flag possible duplicates but must not automatically reject legitimate new versions.
- Active workflows preserve the document versions used in their decisions.

## Version Types

| Type | Rule |
| --- | --- |
| Uploaded evidence | New file creates a new version or separate evidence record. |
| Corrected submission | Must link to returned/deficient version and reason. |
| Updated credential | Prior credential remains retained/superseded. |
| Generated report | Released reports are versioned snapshots. |
| Appointment document | Corrections create new official versions. |
| Policy issuance | Supersession preserves old version and effectivity. |
| Template | Template versions are separate from generated documents. |
| Signed document | Immutable; corrections require new signed version. |
