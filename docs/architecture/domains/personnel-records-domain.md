# Personnel Records Domain

## Purpose

Own 201 files, employee documents, document versions, verification, access logs, retention classification, archive status, and document history.

## Business Scope

201 File, Document Type, Employee Document, Document Version, Verification, Access Log, Retention Classification, Archive Status, Document History.

## Out of Scope

Structured employee data ownership, appointment decisions, assessment scoring, and policy interpretation.

## Main Entities

201 File, Document Type, Employee Document, Document Version, Verification, Access Log, Retention Classification, Archive Status, Document History.

## Aggregate or Ownership Candidates

Employee 201 file, document record, document version, verification record, access log.

## Key Business Rules

- Uploaded documents are evidence records, not substitutes for structured HR data.
- Document access must be logged.
- Verification and retention rules must be policy-configurable.
- Documents may support many workflows but remain owned by Personnel Records.

## Commands or Use Cases

Create 201 file, upload document reference, verify document, replace document version, record access, archive document.

## Domain Events

EmployeeDocumentUploaded, DocumentVerified, DocumentVersionCreated, DocumentAccessed, DocumentArchived.

## Dependencies

Depends on Workforce, Core Platform, Policy and Configuration, and Organization. Provides evidence references to all HR domains.

## Policy Dependencies

Government records management, Data Privacy Act, DepEd records rules, CSC personnel records.

## Security Sensitivity

Restricted.

## Audit Requirements

Log upload, verification, rejection, replacement, view, download, archive, retention action, and restricted access.

## Reports Produced

201 file completeness report, verification queue, access log report, retention due report, document history report.

## Implementation Phase

Phase 3.
