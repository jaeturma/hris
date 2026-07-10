# Attendance Domain

## Purpose

Own attendance logs, biometric imports, schedules, holidays, official business, travel orders, overtime, undertime, adjustments, and DTR records.

## Business Scope

Attendance Log, Biometric Log, Work Schedule, Holiday, Official Business, Travel Order, Overtime, Undertime, Attendance Adjustment, DTR.

## Out of Scope

Leave credit ownership, payroll computation, employee master data, and device adapter implementation.

## Main Entities

Attendance Log, Biometric Log, Work Schedule, Holiday, Official Business, Travel Order, Overtime, Undertime, Attendance Adjustment, DTR.

## Aggregate or Ownership Candidates

Attendance day record, DTR, attendance adjustment, work schedule.

## Key Business Rules

- Imported data must be distinguishable from computed, adjusted, and approved data.
- Adjustments require approval and audit history.
- Attendance consumes approved leave and official business records but does not own leave rules.

## Commands or Use Cases

Import attendance logs, generate DTR, submit attendance adjustment, approve adjustment, reconcile leave, export attendance inputs.

## Domain Events

AttendanceLogImported, DtrGenerated, AttendanceAdjustmentSubmitted, AttendanceAdjustmentApproved, AttendanceReconciled.

## Dependencies

Depends on Workforce, Organization, Policy and Configuration, Leave, Personnel Records, and Integration. Feeds Payroll Preparation.

## Policy Dependencies

CSC attendance rules, DepEd local attendance procedures, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log imports, matching, DTR generation, adjustments, approvals, and payroll-preparation exports.

## Reports Produced

DTR, tardiness report, undertime report, absence report, adjustment report, attendance summary.

## Implementation Phase

Phase 9.
