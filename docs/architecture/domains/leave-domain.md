# Leave Domain

## Purpose

Own leave types, leave credits, leave ledgers, applications, approvals, leave without pay, monetization readiness, and terminal leave readiness.

## Business Scope

Leave Type, Leave Credit, Leave Ledger, Leave Application, Leave Approval, Leave Without Pay, Monetization Readiness, Terminal Leave Readiness.

## Out of Scope

Attendance log ownership, payroll disbursement, employee master data, and performance evaluation.

## Main Entities

Leave Type, Leave Credit, Leave Ledger, Leave Application, Leave Approval, Leave Without Pay, Monetization Readiness, Terminal Leave Readiness.

## Aggregate or Ownership Candidates

Leave ledger, leave application, leave credit balance, leave approval.

## Key Business Rules

- Leave rules are separate from attendance calculations but integrate with DTR and payroll preparation.
- Ledger changes require audit-safe history.
- Sensitive leave documents remain protected by Personnel Records.

## Commands or Use Cases

Apply for leave, approve leave, deny leave, adjust leave credit, post ledger entry, compute terminal leave readiness.

## Domain Events

LeaveApplied, LeaveApproved, LeaveDenied, LeaveLedgerPosted, LeaveCreditAdjusted.

## Dependencies

Depends on Workforce, Organization, Policy and Configuration, Personnel Records, and Core Platform. Feeds Attendance and Payroll Preparation.

## Policy Dependencies

CSC leave rules, DepEd leave administration practices, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log applications, approvals, denials, cancellations, ledger adjustments, and document access.

## Reports Produced

Leave ledger, leave balance report, pending leave report, leave without pay report, terminal leave readiness report.

## Implementation Phase

Phase 9.
