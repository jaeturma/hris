# Appointment and Personnel Action Domain

## Purpose

Own appointment issuance, assumption, CSC submission/action tracking, and internal personnel action history.

## Business Scope

Appointment Recommendation, Appointment, Assumption, CSC Submission, CSC Action, Transfer, Reassignment, Detail, Designation, Promotion, Demotion, Separation, and Personnel Action History.

## Out of Scope

Recruitment evaluation, applicant ranking, career progression assessment, leave ledger, attendance calculations, and payroll disbursement.

## Main Entities

Appointment Recommendation, Appointment, Assumption, CSC Submission, CSC Action, Personnel Movement, Transfer, Reassignment, Detail, Designation, Promotion, Demotion, Separation, Personnel Action History.

## Aggregate or Ownership Candidates

Appointment, CSC action tracker, personnel movement, personnel action history.

## Key Business Rules

- Some actions originate from Recruitment; others arise from internal personnel administration.
- Appointment lifecycle is separate from selection recommendation.
- Personnel actions must update service records and plantilla occupancy through controlled workflows.
- CSC submission and returned-action history must be preserved.

## Commands or Use Cases

Prepare appointment, issue appointment, record assumption, submit to CSC, record CSC action, record transfer, record reassignment, record separation.

## Domain Events

AppointmentPrepared, AppointmentIssued, AssumptionRecorded, CscSubmissionSent, CscActionRecorded, PersonnelMovementRecorded, SeparationRecorded.

## Dependencies

Depends on Workforce, Plantilla and Position, Organization, Policy and Configuration, Recruitment, Career Progression, Personnel Records, and Core Platform.

## Policy Dependencies

CSC ORAOHRA, DepEd appointment/personnel action guidance, Agency MSP, records management, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log appointment preparation, issuance, assumption, CSC submission, returned action, movement, separation, and service-record-triggering changes.

## Reports Produced

Appointment tracker, CSC submission log, personnel movement report, separation report, action history report.

## Implementation Phase

Phase 4 to 7, beginning with appointment tracking after recruitment foundation.
