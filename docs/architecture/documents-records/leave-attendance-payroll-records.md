# Leave, Attendance, and Payroll-Preparation Records

## Purpose

Define records for leave, attendance, DTR, official business, travel, overtime, and payroll-preparation inputs.

## Record Types

Leave application, supporting medical or legal documents, leave approval, leave ledger, Daily Time Record, attendance adjustment, Official Business, Travel Order, overtime authorization, work schedule, payroll adjustment input, Leave Without Pay certification, and payroll-preparation export.

## Temporary Inputs vs Official Records

| Record | Temporary Input or Official Record |
| --- | --- |
| Raw biometric import | Temporary/input until reconciled. |
| Work schedule | Active reference record. |
| Attendance adjustment request | Workflow record; final if approved/rejected. |
| DTR | Official generated record when finalized. |
| Leave application | Official workflow record after submission/finalization. |
| Medical/legal support | Restricted evidence record. |
| Leave ledger | Structured source of truth for leave balances. |
| Payroll adjustment input | Payroll-preparation input snapshot. |
| Payroll export | Official export snapshot when released. |

## Rules

- Leave rules remain separate from attendance calculations.
- Payroll preparation consumes snapshots; it must not rewrite leave or attendance records.
- Medical or legal leave support requires restricted handling.
- DTR and payroll exports must preserve generation parameters and source snapshots.
