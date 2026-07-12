# Workflow, Event, and Notification Readiness

## Readiness matrix

| Capability | Current architecture | Needed before implementation | Status |
|---|---|---|---|
| State vocabulary/instances | defined conceptually | concrete first-workflow states and invariants | Amber |
| Assignment/routing | role/office/actor concepts | sequential/parallel/recusal/reassignment rules | Amber by module |
| Versioning/snapshots | required | activation and in-flight behavior | Amber |
| Domain events | past-tense facts, stable IDs | per-aggregate event contracts | Amber |
| Notifications | separate from truth; channels staged | preference, template and delivery ownership | Amber |
| Queues/retries | idempotency and observability principles | backend, retry/dead-letter runbook | Amber |
| Deadlines/escalation | conceptual | policy-validated clock/calendar/rule | Red by affected workflow |
| HRMPSB deliberation | explicitly specialized | quorum, recusal, deliberation and authority validation | Red until policy validation |

## Implementation rule

Start with identifiers, concrete workflow records, assignment authorization and audit for the first approved use case. Extract repeated transition and assignment patterns only after evidence from multiple workflows. Do not build an unrestricted designer or universal personnel-action workflow.

Events name completed facts in past tense, carry stable identifiers and minimal sensitive payloads. Listeners and queued jobs are idempotent. Retry and failure are observable. Integration events cannot bypass the initiating authorization. Notification delivery failure does not undo a valid domain transaction.

## Test requirements

Test allowed/forbidden transitions, optimistic concurrency, duplicate commands/events, retry safety, stale version behavior, sequential and parallel review, reassignment/delegation/recusal, deadline boundaries, closed-case access, notification failure independence, and complete audit chronology.

**Assessment: Amber for foundation design; Red for policy-specific workflows until validated.**

