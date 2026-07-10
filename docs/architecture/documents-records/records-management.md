# Records Management

## Purpose

Define records-management architecture for active, semi-active, inactive, permanent, temporary, archived, disposition-ready, legal-hold, investigation-hold, and audit-hold records.

## Record Statuses

| Status | Meaning | Handling |
| --- | --- | --- |
| Active record | Currently used in operations. | Accessible to authorized workflow users. |
| Semi-active record | Used occasionally for reference. | Lower operational visibility; still retained. |
| Inactive record | No longer used for regular operations. | Archive-ready or retained by schedule. |
| Permanent record | Must be preserved permanently when verified by schedule. | Never dispose through ordinary workflow. |
| Temporary record | Short-term processing or temporary support file. | Disposition by configured rule after validation. |
| Archived record | Transferred to archive status/storage. | Records custodian access. |
| Disposition-ready record | Eligible for disposition review. | Requires human approval before action. |
| Legal-hold record | Subject to legal hold. | Disposition suspended. |
| Investigation-hold record | Subject to investigation. | Disposition suspended and access restricted. |
| Audit-hold record | Needed for audit. | Disposition suspended until release. |

## Required Metadata

Records series, retention category, retention period, disposition authority, office of record, custodian, owner, physical-location reference, digital-storage reference, archive transfer, legal or audit hold, disposition approval, disposition certificate, and destruction or transfer evidence.

## Rules

- Do not hardcode retention periods unless verified by an applicable official schedule.
- Retention must be policy-driven and versioned.
- The system must not automatically destroy official government records.
- Holds suspend disposition.
- Records linked to unresolved cases or audits must not be disposed.
- Disposition history must be immutable.

## Offices and Custodians

Each record must identify office of record, source office, responsible custodian, and owning domain. Custodian authority is not the same as domain business ownership.
