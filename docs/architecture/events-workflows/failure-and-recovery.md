# Failure and Recovery

## Purpose

Define recovery procedures for workflow, queue, notification, policy, document, and integration failures.

| Failure | Recovery Procedure | Audit Requirement |
| --- | --- | --- |
| Queue failure | Mark job failed, preserve payload reference, allow safe manual replay. | Failed job log, replay actor, result. |
| Notification failure | Retry channel; keep in-app notification; workflow remains unchanged. | Delivery failure log. |
| Partial workflow completion | Preserve completed steps; create recovery task for incomplete side effects. | Recovery action log. |
| External service outage | Pause integration job; use manual fallback where available. | Outage and retry log. |
| Duplicate submission | Detect idempotency key; return existing result or route to manual review. | Duplicate detection log. |
| Stale assignment | Check current assignment at action time; require reassignment if expired. | Reassignment log. |
| Approver unavailable | Use delegated/acting authority only if configured and valid. | Delegation/acting capacity log. |
| Invalid workflow configuration | Block new starts; active workflows preserve prior version; escalate to admin. | Configuration error log. |
| Policy superseded during active workflow | Preserve starting policy unless authorized transition rule applies. | Transition decision log. |
| Document processing failure | Mark processing failed; keep document pending manual review. | Processing failure log. |
| Report generation failure | Retry if safe; preserve failed report job. | Report failure log. |
| Integration timeout | Retry with idempotency; route unresolved item to reconciliation. | Timeout and reconciliation log. |

## Active Workflow Rule

Active workflows preserve the policy and workflow versions under which they started unless an authorized migration or transition rule explicitly applies.
