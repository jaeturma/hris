# Personnel Master Data

## Purpose

Define the core employee data architecture for identity, personal information, employment information, assignments, movements, and service records.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `employees` | Primary employee identity record. | `id`, `employee_number`, `uuid`, `last_name`, `first_name`, `middle_name`, `name_extension`, `status` | Parent of employee detail tables | no | high |
| `employee_personal_information` | Sensitive personal profile details. | `id`, `employee_id`, `birth_date`, `sex`, `civil_status`, `contact_number`, `address`, `emergency_contact` | Parent `employees` | no | high |
| `employee_employment_information` | Government employment details. | `id`, `employee_id`, `employment_status_id`, `original_appointment_date`, `government_service_start_date`, `tin`, `gsis`, `pagibig`, `philhealth` | Parent `employees`, `employment_statuses` | no | high |
| `employee_assignments` | Current and historical assignment records. | `id`, `employee_id`, `station_id`, `office_id`, `position_title_id`, `plantilla_item_id`, `start_date`, `end_date`, `is_current` | Parents `employees`, `stations`, `plantilla_items` | no | high |
| `employee_movements` | Appointment, transfer, promotion, reclassification, separation, and other movements. | `id`, `employee_id`, `movement_type`, `from_station_id`, `to_station_id`, `effective_date`, `source_record_type`, `source_record_id` | Parents `employees`, `stations`; source workflow records | no | high |
| `employee_service_records` | Official service history entries. | `id`, `employee_id`, `from_date`, `to_date`, `designation`, `status`, `salary`, `station_id`, `source_movement_id` | Parents `employees`, `employee_movements` | no | high |

## Main Fields

Use employee identifiers, effective dates, source references, current flags, status fields, office scope, created/updated/approved metadata, and correction history references.

## Relationships

`employees` is the core parent. Personal and employment information are one-to-one or versioned detail tables. Assignments and service records are historical. Movements should feed assignment and service record updates after approval.

## Indexing Considerations

Index `employee_number`, `uuid`, names for search, current assignment fields, `station_id`, `office_id`, `plantilla_item_id`, `effective_date`, and `is_current`.

## Data Ownership

Owned by HR and records officers. Employees may view selected own-profile data if policy permits.

## Data Visibility Rules

Restrict personal, government ID, 201 file, service record, and movement details to authorized HR, records, supervisors, auditors, or the employee where allowed.

## Audit Requirements

Audit all changes to personal information, employment information, assignments, movements, and service records. Preserve correction history.

## Seeder Requirements

No employee records should be seeded in production. Use anonymized factory data only for local/testing.

## Notes Before Migration Creation

Decide which employee fields are versioned. Confirm whether government identifiers should be encrypted or masked in application display.
