# Event, Workflow, and Notification Architecture

This folder defines the event-driven, workflow, approval, escalation, queue, and notification architecture for HRIS for DepEd.

This is documentation only. Do not create Laravel events, listeners, jobs, notifications, services, routes, migrations, models, policies, controllers, or React components from this folder until an implementation phase explicitly authorizes code.

## Purpose

Support DepEd hiring, appointment, HRMPSB, promotion, reclassification, expanded career progression, competency-based HRM, leave, attendance, personnel actions, approvals, immutable history, escalations, and notifications without making every operation asynchronous.

## Architecture Decisions

1. Project remains HRIS for DepEd.
2. DepEd-specific workflows are primary.
3. CSC rules and frameworks provide government-wide alignment.
4. Workflow definitions are versioned.
5. Active workflows preserve their applicable policy version.
6. Domain events represent completed facts.
7. Notifications do not control business truth.
8. Approval decisions remain synchronous and attributable.
9. Long-running side effects may use queues.
10. Failed notifications do not reverse approved actions.
11. HRMPSB assignments are cycle-specific.
12. Sensitive notifications expose minimal information.
13. Workflow state transitions require authorization and validation.
14. Major workflow decisions use structured immutable history.
15. AI cannot directly approve, reject, rank, appoint, or alter official records.

## File Map

| File | Purpose |
| --- | --- |
| `architecture-principles.md` | Event, workflow, queue, approval, and AI rules. |
| `domain-event-catalog.md` | Domain event catalog by major domain. |
| `workflow-engine.md` | Configurable workflow engine concepts. |
| `approval-routing.md` | Approval and deliberation routing patterns. |
| `workflow-state-model.md` | Standard states, transitions, guards, and corrections. |
| `notification-architecture.md` | Multi-channel notification architecture. |
| `escalation-and-deadlines.md` | Deadline types, reminders, escalation, and overrides. |
| `audit-and-immutability.md` | Structured history and immutable decision records. |
| `queue-and-job-strategy.md` | Queue use, priorities, retries, and monitoring. |
| `idempotency-and-retries.md` | Duplicate handling and retry safety. |
| `security-and-data-scope.md` | Workflow authorization and data scope rules. |
| `integration-events.md` | Future external integration events. |
| `event-payload-standards.md` | Payload schema and sensitivity rules. |
| `workflow-catalog.md` | Workflow catalog for HRIS processes. |
| `notification-catalog.md` | Notification catalog. |
| `failure-and-recovery.md` | Recovery procedures. |
| `testing-strategy.md` | Future Pest testing strategy. |
| `implementation-roadmap.md` | Staged implementation plan. |
| `event-workflow-matrix.md` | Representative action matrix. |

## Boundary Rule

Events, workflows, queues, and notifications support domain rules. They do not replace domain ownership, policy configuration, authorization, audit history, or human accountability.
