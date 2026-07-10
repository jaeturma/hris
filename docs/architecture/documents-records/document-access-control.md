# Document Access Control

## Purpose

Define access controls for preview, download, print, export, release, archive, and disposition actions.

## Access Factors

Role permission, policy authorization, office scope, employee ownership, applicant ownership, workflow assignment, HRMPSB cycle assignment, records-custodian authority, restricted-record permission, temporary access grant, legal or audit hold, delegated access, download permission, print permission, and export permission.

## Preferred Permissions

- `view employee documents`
- `view restricted personnel documents`
- `verify applicant documents`
- `download appointment documents`
- `release official records`
- `archive documents`
- `approve disposition`
- `validate digital signatures`

Avoid generic permissions such as `view all documents`.

## Access Rules

- Every preview, download, print, external share, and restricted-record access should be auditable where appropriate.
- File URLs must never bypass application authorization.
- Temporary URLs must be short-lived and permission-checked before generation.
- Applicant self-service is limited to own applicant documents.
- Employee self-service is limited to own allowable documents.
- HRMPSB and evaluator access is limited to assigned cycles and records.
- Auditors are read-only unless separately authorized.
