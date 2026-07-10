# Architecture Principles

## Core Principles

1. Domain events represent facts that already happened.
2. Commands represent requested actions.
3. Workflow state changes must be explicit.
4. Human approval steps must never be hidden inside background jobs.
5. Sensitive decisions require attributable users and timestamps.
6. Completed workflow decisions must preserve immutable history.
7. Notifications are side effects, not the source of truth.
8. Failed notification delivery must not reverse the underlying approved business action.
9. Policy rules must come from the Policy and Configuration Domain.
10. Cross-domain communication should prefer events or defined application services.
11. Avoid event chains that are difficult to trace.
12. Avoid using events for simple internal method calls.
13. External integrations must use integration events or adapters.
14. Queued jobs must be idempotent where retries are possible.
15. Every workflow must support cancellation, rejection, return, and correction where policy permits.
16. Every major workflow state change must be auditable.
17. Notifications must respect office scope and permission boundaries.
18. Applicants and employees must receive only information appropriate to their role and record ownership.
19. AI-generated recommendations must never directly approve or reject an HR action.
20. Digital signatures must remain attributable to the authorized human signatory.

## Command vs Event

| Type | Meaning | Example |
| --- | --- | --- |
| Command | A request to do something. It may fail validation. | `SubmitApplication`, `ApproveLeave`, `FinalizeEvaluation` |
| Domain Event | A business fact that already happened. | `ApplicationSubmitted`, `LeaveApplicationApproved`, `EvaluationFinalized` |
| Workflow Event | A workflow movement fact. | `WorkflowStepCompleted`, `WorkflowReturned` |
| Notification Event | A communication side effect. | `NotificationRequested`, `NotificationDelivered` |
| Integration Event | A boundary event for external systems. | `PayrollExportGenerated`, `DigitalSignatureRequested` |

## Synchronous vs Asynchronous

Keep authorization, validation, workflow transitions, approvals, rejections, data integrity checks, and critical audit records synchronous. Use queues for side effects, large processing, exports, integration sync, reminders, and document processing.

## Policy Rule

Policy versions, assessment framework versions, Merit Selection Plan versions, qualification-standard versions, competency-framework versions, and workflow definition versions must be resolved before a workflow action is accepted.
