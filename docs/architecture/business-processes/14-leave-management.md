# 14 Leave Management

## Purpose

Manage leave credits, applications, approvals, ledger entries, supporting documents, and reporting for employees.

## Trigger

Employee leave application, leave credit adjustment, HR ledger correction, supervisor action, or payroll preparation requirement.

## Actors

Employee, immediate supervisor, school or office head, HR leave administrator, approving authority, payroll preparer, auditor.

## Inputs

Employee record, leave type, leave credits, application dates, supporting documents, work schedule, holidays, approval path, and ledger entries.

## High-Level Process Flow

1. Employee submits leave application or HR records manual entry.
2. System checks leave type, available credits, schedule, conflicts, and required documents.
3. Route to supervisor and approving authority.
4. Record approval, disapproval, cancellation, or return for correction.
5. Update leave ledger and related payroll preparation records.
6. Preserve documents and audit trail.

## Decision Points

- Is the leave type applicable and supported by required documents?
- Are credits sufficient or is special handling required?
- Which supervisor or approving authority applies?
- Does the leave affect payroll preparation or attendance?

## Outputs

Leave application, approval history, leave ledger entry, leave balance, payroll preparation note, leave reports.

## Applicable Policy Area

CSC leave rules; DepEd local leave administration practices; Data Privacy Act; records management.

## PRIME-HRM Contribution

Supports HR operations and employee welfare evidence related to performance and records integrity.

## Competency-Based HRM Link

Leave data may contextualize performance and L&D scheduling but should not be misused for competency judgment.

## System Responsibilities

Maintain leave balances, approval routing, ledger integrity, document linkage, correction history, and audit logs.

## Automation Opportunity Rating

Very High - balance checks, routing, reminders, ledgers, and reports are repeatable.

## AI Readiness Rating

Medium - AI can answer policy-aware status questions and summarize trends, but leave eligibility decisions must follow configured rules.

## AI Opportunities

Leave balance explanations, missing document alerts, recurring absence pattern summaries, and supervisor workload summaries.

## Reports Produced

Leave ledger, leave application report, pending approvals, leave balance report, leave utilization summary.

## Security Considerations

Protect health-related or sensitive leave documents; restrict approvals and ledger adjustments; audit all corrections.

## Future Integrations

Attendance Devices, Payroll, Document Management, Email, SMS, Mobile Application, AI Assistant.

## Related Business Processes

Attendance Timekeeping, Personnel Records, Payroll Preparation, Performance Management.
