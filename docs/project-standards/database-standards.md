# Database Standards

Database design must support long-lived, auditable government HR records at regional, division, district, school, and implementing-unit scale.

## Keys and IDs

- Use Laravel default big integer primary keys unless a module has a documented reason for UUID primary keys.
- Use UUIDs for public identifiers, import batches, audit correlation, or external references when enumeration risk exists.
- Do not expose sequential IDs in sensitive public-facing contexts without authorization.

## Foreign Keys and Indexes

- Add foreign keys for required relationships.
- Index common filters such as office scope, status, effective date, item number, employee number, and approval state.
- Use composite indexes for frequent combined filters, for example `division_id + status` or `employee_id + effective_date`.
- Avoid cascading deletes on official HR records unless explicitly justified.

## Timestamps and Audit Columns

- Use `created_at` and `updated_at` on normal records.
- Add `created_by`, `updated_by`, `approved_by`, `rejected_by`, `cancelled_by`, or `exported_by` where the business process needs explicit attribution.
- Use effective dates for appointments, promotions, transfers, separations, service records, and leave records.
- Do not rely on timestamps alone for official history.

## Soft Deletes

- Use soft deletes for administrative records that may need recovery.
- Avoid soft deletes as a substitute for official correction workflows.
- Do not hard-delete personnel records, 201 file metadata, service records, or personnel actions unless a documented retention rule allows it.

## Reference and Lookup Tables

- Use lookup tables for values that may change through policy or configuration.
- Use enums for stable internal states that are unlikely to change.
- Keep salary grades, position titles, and plantilla-related references distinct.

## Nullable Columns

- Make columns nullable only when the domain permits unknown, pending, or not-applicable values.
- Document why important government HR fields may be nullable.
- Prefer explicit statuses over using `null` as a workflow state.

## Naming and Constraints

- Use plural snake_case table names.
- Use clear foreign key names such as `employee_id`, `school_id`, and `plantilla_item_id`.
- Add unique constraints for true business rules, such as item number uniqueness within the correct scope.
- Validate in both application code and database constraints where possible.
