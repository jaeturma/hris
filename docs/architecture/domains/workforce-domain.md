# Workforce Domain

## Purpose

Own employee identity and the employment relationship for DepEd HR operations.

## Business Scope

Employee, employee number, personal information, employment profile, current assignment reference, employment status, work history, workforce status, and separation status.

## Out of Scope

Recruitment applications, leave balances, attendance calculations, payroll preparation, appointment approval, and 201 file document verification.

## Main Entities

Employee, Employee Number, Personal Information, Employment Profile, Current Assignment, Employment Status, Work History, Workforce Status, Separation Status.

## Aggregate or Ownership Candidates

Employee aggregate, employment profile, workforce status history.

## Key Business Rules

- Employee represents personnel identity and employment relationship.
- Current assignment references Organization and Plantilla/Position data but does not own those domains.
- Employee identity must be preserved across movements, appointments, and separations.
- Sensitive personal information requires office-scope and purpose-based access.

## Commands or Use Cases

Create employee, update personal information, update employment profile, change workforce status, mark separated.

## Domain Events

EmployeeCreated, EmployeeProfileUpdated, WorkforceStatusChanged, EmployeeSeparated.

## Dependencies

Depends on Organization, Core Platform, Appointment and Personnel Action, and Personnel Records. Provides employee references to most HR domains.

## Policy Dependencies

CSC personnel rules, DepEd personnel administration, Data Privacy Act, records management.

## Security Sensitivity

High.

## Audit Requirements

Log creation, personal data changes, employment status changes, separation status, and sensitive field access.

## Reports Produced

Employee masterlist, workforce status report, employment profile report, separation status report.

## Implementation Phase

Phase 1 after Organization and Core Platform.
