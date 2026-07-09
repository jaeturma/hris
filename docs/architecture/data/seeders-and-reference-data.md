# Seeders and Reference Data

## Purpose

Define the reference data strategy for safe, verified seeders in a government-grade DepEd HRIS.

## Seeder Principles

- Seed stable reference data only after manual verification.
- Do not seed real employee, applicant, or sensitive document records in production.
- Keep office-specific or policy-changing values configurable.
- Use import workflows for large masterlists such as schools, plantilla items, and competency libraries.
- Track source, verification date, and policy reference for seeded government data.

## Proposed Seeder Groups

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `regions` | Official regions. | `code`, `name`, `is_active` | Parent of divisions | yes | low |
| `divisions` | Official divisions. | `region_id`, `code`, `name`, `is_active` | Parent of districts/schools | yes | low |
| `schools` | Official school list. | `division_id`, `school_id_number`, `name`, `is_active` | Used by stations/employees | yes/import | medium |
| `position_titles` | Official position titles. | `code`, `name`, `position_group`, `is_active` | Plantilla and appointments | yes | medium |
| `salary_grades` | Salary grade schedule. | `grade`, `step`, `amount`, `effective_from` | Plantilla and appointments | yes | medium |
| `employment_statuses` | Employment status references. | `code`, `name`, `is_active` | Employees/appointments | yes | medium |
| `appointment_statuses` | Appointment status references. | `code`, `name`, `is_terminal` | Appointments | yes | medium |
| `document_types` | Document type masterlist. | `code`, `name`, `document_group`, `is_sensitive` | Documents | yes | high |
| `leave_types` | Leave type references. | `code`, `name`, `is_credit_based` | Leave records | yes | medium |
| `competency_categories` | Core, leadership, functional/technical categories. | `code`, `name`, `sort_order` | Competencies | yes | low |
| `competency_levels` | Proficiency levels. | `code`, `name`, `level_number` | Indicators/mappings | yes | medium |
| `roles` | RBAC role references. | `name`, `guard_name` | Spatie permissions | yes | high |
| `permissions` | RBAC permission references. | `name`, `guard_name` | Spatie roles | yes | high |

## Main Fields

Seedable tables should include stable codes, names, active flags, sort order, source reference, verification date, and effective dates where applicable.

## Relationships

Seed parent references before dependent references: organization hierarchy, then position/salary, then document/leave/competency/security references.

## Indexing Considerations

Unique codes should be indexed. Add parent-code composite indexes when codes are only unique inside a parent scope.

## Data Ownership

Owned by system administrators and HR governance owners. Source verification should be assigned before production seed/import.

## Data Visibility Rules

Most seeded references are readable by authorized HR users. Role, permission, document sensitivity, and approval flow seed data should be admin-only.

## Audit Requirements

Seeder/import runs should be logged with source, actor, timestamp, records created/updated, and verification status.

## Notes Before Migration Creation

Prepare seeders only after deciding source of truth, update frequency, and whether values are global or office-specific.
