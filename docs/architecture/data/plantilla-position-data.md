# Plantilla and Position Data

## Purpose

Define position, plantilla, salary, job family, employment status, and appointment reference data for DepEd-first HR operations and competency mapping.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `position_titles` | Official position title masterlist. | `id`, `code`, `name`, `position_group`, `is_teaching`, `is_active` | Used by `plantilla_items`, `employee_assignments` | yes | medium |
| `plantilla_items` | Authorized plantilla item records. | `id`, `item_number`, `position_title_id`, `salary_grade_id`, `station_id`, `status`, `funding_source`, `effective_date` | Parents `position_titles`, `salary_grades`, `stations` | yes/import | high |
| `salary_grades` | Salary grade reference data. | `id`, `grade`, `step`, `amount`, `effective_from`, `effective_to` | Used by `plantilla_items`, `appointments` | yes | medium |
| `job_families` | CBHRMS job family grouping. | `id`, `code`, `name`, `description`, `is_active` | Used by position competency profiles | yes | medium |
| `employment_statuses` | Employment status reference. | `id`, `code`, `name`, `description`, `is_active` | Used by employee employment and appointments | yes | medium |
| `appointment_statuses` | Appointment status reference. | `id`, `code`, `name`, `description`, `is_terminal`, `is_active` | Used by appointments | yes | medium |

## Main Fields

Position data should include official code/name, salary grade, item number, station, funding/source metadata, status, effective dates, and links to competency profiles.

## Relationships

Plantilla items belong to position titles, salary grades, and stations. Job families group position titles or position profiles. Appointment records should reference plantilla and salary data as of appointment time.

## Indexing Considerations

Unique or heavily index `item_number`, `position_title_id`, `salary_grade_id`, `station_id`, `status`, and effective-date ranges.

## Data Ownership

Owned by HR plantilla administrators and authorized regional/division staff.

## Data Visibility Rules

General position and salary grade references may be visible to HR users. Item occupancy, funding, and movement-sensitive data should be restricted.

## Audit Requirements

Audit plantilla item status, station, salary grade, title changes, and job family/competency mapping changes.

## Seeder Requirements

Seed verified position titles, salary grades, employment statuses, appointment statuses, and job families. Plantilla items should usually be imported from verified official data.

## Notes Before Migration Creation

Confirm item number uniqueness scope, salary schedule versioning, and how reclassification affects plantilla item history.
