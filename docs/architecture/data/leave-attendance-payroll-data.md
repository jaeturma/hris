# Leave, Attendance, and Payroll Preparation Data

## Purpose

Define data for leave management, attendance, DTR, work schedules, holidays, payroll preparation, and future attendance device/payroll export integration.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `leave_types` | Leave type reference. | `id`, `code`, `name`, `is_credit_based`, `is_active` | Used by leave tables | yes | medium |
| `leave_credits` | Employee leave credit balances. | `id`, `employee_id`, `leave_type_id`, `balance`, `as_of_date` | Parents employees, leave types | no | high |
| `leave_applications` | Leave requests and approvals. | `id`, `employee_id`, `leave_type_id`, `date_from`, `date_to`, `status`, `approved_by` | Parents employees, leave types | no | high |
| `leave_ledger_entries` | Leave credit ledger movements. | `id`, `employee_id`, `leave_type_id`, `entry_date`, `credit`, `debit`, `source_type`, `source_id` | Parents employees, leave types | no | high |
| `work_schedules` | Employee or office work schedules. | `id`, `scheduleable_type`, `scheduleable_id`, `name`, `start_time`, `end_time`, `effective_from` | Polymorphic office/employee parent | yes/config | medium |
| `holidays` | Holiday reference by scope. | `id`, `holiday_type_id`, `date`, `name`, `scope_type`, `scope_id` | Parent holiday types and offices | yes/import | low |
| `attendance_logs` | Raw attendance device or encoded logs. | `id`, `employee_id`, `source`, `logged_at`, `log_type`, `device_reference` | Parent employees; integration source | no | high |
| `attendance_adjustments` | Corrections to attendance logs. | `id`, `employee_id`, `attendance_log_id`, `adjustment_type`, `reason`, `approved_by` | Parents employees/logs | no | high |
| `dtr_records` | Daily time record summaries. | `id`, `employee_id`, `period_start`, `period_end`, `status`, `generated_at` | Parent employees, attendance logs | no | high |
| `payroll_periods` | Payroll preparation periods. | `id`, `period_code`, `date_from`, `date_to`, `status` | Parent payroll prep records | yes/config | medium |
| `payroll_preparation_records` | Payroll export preparation data. | `id`, `employee_id`, `payroll_period_id`, `gross_reference`, `deduction_reference`, `status` | Parents employees, payroll periods | no | high |

## Main Fields

Use employee, period, date/time, source, status, approver, device reference, export batch, and correction reason fields.

## Relationships

Leave applications feed ledger entries after approval. Attendance logs feed DTR records. Payroll preparation records depend on employees, assignments, attendance, leave, and payroll periods.

## Indexing Considerations

Index employee/date ranges, leave type/status, attendance timestamp/source, DTR period/status, payroll period/status, and device references.

## Data Ownership

Owned by HR leave administrators, timekeepers, payroll preparation staff, and authorized office administrators.

## Data Visibility Rules

Leave balances, attendance, DTR, and payroll preparation data are sensitive. Limit to authorized HR, timekeeper, payroll staff, supervisors, auditors, and employee self-view where allowed.

## Audit Requirements

Audit leave approvals, ledger changes, attendance adjustments, DTR finalization, and payroll export preparation.

## Seeder Requirements

Seed leave types, holiday types, baseline work schedules, and payroll periods only after policy and office calendar verification.

## Notes Before Migration Creation

Confirm attendance device data format, payroll export format, leave credit rules, and holiday source of truth.
