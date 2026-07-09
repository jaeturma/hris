# Database Rules

The database is the authoritative record store for a government-grade DepEd HRIS. Use MySQL-compatible schema design and preserve historical HR records.

## Modeling Principles

- Use relational tables for core HR data.
- Model Region, Division, District, School, and Implementing Unit explicitly.
- Keep office scoping clear on sensitive records.
- Use foreign keys where relationships must be enforced.
- Add indexes for office scope, status, effective dates, item numbers, employee IDs, and common filters.
- Prefer immutable historical rows for personnel actions instead of overwriting prior state.

## Core Data Concepts

Future schema design must distinguish Employee personal profile, government employment details, Plantilla Item, Position Title, Salary Grade, Item Number, Appointment, Promotion, Reclassification, Transfer, Separation, Service Record, leave records, 201 file metadata, recruitment and HRMPSB records, and Performance Rating. Do not merge these into one oversized employee table.

## Auditability

- Tables that represent official HR actions should include effective dates and status fields.
- Store who created, updated, approved, rejected, cancelled, or exported records where applicable.
- Use Spatie Laravel Activitylog for user-facing audit trails.
- Do not rely only on `updated_at` for official history.
- Avoid hard deletes for official personnel records unless a retention or correction policy explicitly allows it.

## Migrations

- Migrations must be reversible where practical.
- Use clear column names and avoid ambiguous abbreviations.
- Add constraints for required domain invariants.
- Store monetary or numeric government values with appropriate precision.
- Use enums or lookup tables carefully; prefer lookup tables for policy-managed values that can change.

## Sensitive Data

- Minimize personal data fields.
- Protect 201 file references and attachments.
- Do not store secrets, passwords, or private keys in normal HR tables.
- Avoid logging full personal data in activity descriptions, exceptions, or job payloads.

## Data Imports

Bulk imports must be staged, validated, permission-gated, and audit-logged. Import workflows must report row-level errors without exposing private data to unauthorized users.
