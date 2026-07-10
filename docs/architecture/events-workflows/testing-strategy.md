# Testing Strategy

## Purpose

Define future Pest test coverage for events, workflows, notifications, queues, security, and audit behavior. Do not write tests in this phase.

## Pest Test Areas

| Area | Future Pest Coverage |
| --- | --- |
| Event dispatch | Assert domain events are emitted only after successful state changes. |
| Listener behavior | Assert listeners are idempotent and respect domain boundaries. |
| Workflow state transitions | Assert allowed and prohibited transitions. |
| Authorization | Assert permission, office scope, assignment scope, and state checks. |
| Assignment rules | Assert role, user, office, HRMPSB, evaluator, delegated, and acting assignments. |
| Deadline calculation | Assert holidays, non-working days, suspended deadlines, grace periods. |
| Escalation | Assert reminders and escalations are generated at correct levels. |
| Notification recipients | Assert only authorized recipients receive notifications. |
| Notification content sensitivity | Assert SMS/email omit restricted data. |
| Idempotency | Assert duplicate actions do not duplicate approvals or personnel actions. |
| Retries | Assert retry-safe jobs do not corrupt workflow state. |
| Queue failure | Assert workflow truth is preserved when queued side effects fail. |
| Policy version preservation | Assert active workflows preserve policy/workflow versions. |
| Immutable audit history | Assert finalized decisions create structured immutable records. |
| Office data scope | Assert Region/Division/District/School/IU scoping. |
| HRMPSB cycle restrictions | Assert HRMPSB members only access assigned cycles. |

## Test Design Rules

- Use feature tests for workflow behavior.
- Use unit tests for transition guards and deadline calculation.
- Use datasets for workflow states and role/scope combinations.
- Use fake notifications, fake queues, and fake events where appropriate.
- Include negative tests for unauthorized action attempts.
