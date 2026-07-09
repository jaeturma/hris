# Core Reference Tables

## Purpose

Define shared lookup data used across organization, plantilla, recruitment, records, competency, leave, attendance, payroll preparation, security, and reporting modules.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `employment_statuses` | Reference list for employment status classifications. | `id`, `code`, `name`, `description`, `is_active`, `sort_order` | Used by `employee_employment_information`, `appointments` | yes | medium |
| `appointment_statuses` | Appointment processing or appointment nature/status references. | `id`, `code`, `name`, `description`, `is_terminal`, `is_active` | Used by `appointments`, `appointment_recommendations` | yes | medium |
| `document_types` | Masterlist of document categories for applicant and employee records. | `id`, `code`, `name`, `document_group`, `is_sensitive`, `requires_verification` | Used by `submitted_documents`, `employee_documents` | yes | high |
| `holiday_types` | Categories for regular, special, local, and office-specific holidays. | `id`, `code`, `name`, `is_paid`, `is_active` | Used by `holidays` | yes | low |
| `approval_statuses` | Shared status reference for approval workflows. | `id`, `code`, `name`, `is_terminal`, `sort_order` | Used by approval and workflow tables | yes | medium |
| `policy_references` | Internal index of DepEd/CSC source references used by configuration. | `id`, `policy_code`, `title`, `issuing_office`, `effective_date`, `verification_status` | Used by recruitment, promotion, competency configuration | yes | medium |

## Main Fields

Reference tables should generally include `code`, `name`, `description`, `is_active`, `sort_order`, `effective_from`, `effective_to`, `created_by`, `updated_by`, and timestamps where governance matters.

## Relationships

Reference tables should be used by transactional records through foreign keys. Avoid storing free-text status names directly in official workflow tables.

## Indexing Considerations

Index `code`, `is_active`, `sort_order`, and effective-date ranges. Add unique constraints to codes where the reference list is controlled.

## Data Ownership

Owned by system administrators, HR administrators, or records administrators depending on reference type. Policy references should be governed by authorized HR or legal/policy staff.

## Data Visibility Rules

Most reference data is broadly readable to authenticated users. Sensitive document type metadata and policy configuration details should be limited to authorized HR, records, and admin users.

## Audit Requirements

Audit changes to policy references, document types, employment statuses, appointment statuses, and approval statuses because changes can alter workflow behavior.

## Seeder Requirements

Seed only stable, verified references. Mark uncertain or office-specific values as manually configurable rather than hardcoded.

## Notes Before Migration Creation

Confirm whether each reference list should be global, office-specific, effective-dated, or policy-versioned.
