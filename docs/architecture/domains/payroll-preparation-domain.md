# Payroll Preparation Domain

## Purpose

Prepare validated HR inputs for payroll-related processing and export readiness without becoming a full disbursement system in the initial phases.

## Business Scope

Payroll Period, Compensation Reference, Allowance, Deduction, Attendance Adjustment Input, Leave Without Pay Input, Payroll Preparation Record, Payroll Export, Validation Status.

## Out of Scope

Official payroll disbursement, accounting, bank release, and plantilla ownership.

## Main Entities

Payroll Period, Compensation Reference, Allowance, Deduction, Attendance Adjustment Input, Leave Without Pay Input, Payroll Preparation Record, Payroll Export, Validation Status.

## Aggregate or Ownership Candidates

Payroll preparation period, payroll preparation record, payroll export batch.

## Key Business Rules

- Payroll preparation consumes validated HR inputs from Workforce, Plantilla, Leave, and Attendance.
- Export records must preserve source snapshots.
- This domain must not rewrite attendance or leave records.

## Commands or Use Cases

Open payroll period, collect validated inputs, prepare payroll record, validate payroll inputs, generate payroll export.

## Domain Events

PayrollPeriodOpened, PayrollInputCollected, PayrollPreparationValidated, PayrollExportGenerated.

## Dependencies

Depends on Workforce, Plantilla and Position, Attendance, Leave, Policy and Configuration, and Integration.

## Policy Dependencies

DepEd payroll preparation practices, government payroll controls, Data Privacy Act, records management.

## Security Sensitivity

Restricted.

## Audit Requirements

Log input collection, validation, corrections, export generation, and export access.

## Reports Produced

Payroll preparation report, LWOP input report, attendance adjustment input report, validation exception report, export log.

## Implementation Phase

Phase 9 or later.
