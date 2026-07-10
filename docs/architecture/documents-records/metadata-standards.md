# Metadata Standards

## Purpose

Define common metadata and document-type-specific metadata expectations.

## Common Metadata Candidates

Title, document type, document category, owner, subject employee, subject applicant, office of record, source office, related workflow, related application, related appointment, related personnel action, policy reference, confidentiality classification, retention category, date issued, date received, date effective, date expired, verification status, signature status, archive status, version, file hash, language, and remarks.

## Rules

- Avoid requiring every metadata field for every document type.
- Use document-type-specific metadata schemas.
- Metadata changes after finalization must be audited.
- Metadata must never be used to bypass file-level authorization.
- Dates should distinguish issued, received, effective, expired, finalized, signed, released, archived, and disposed dates.

## Ownership

The owning domain defines required metadata. Personnel Records owns document metadata infrastructure. Policy and Configuration owns metadata requirements that are policy-driven.
