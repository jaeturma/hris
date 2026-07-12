# Workflow and Event Implementation Strategy

Implement stable workflow identifiers and audit concepts first, then one approved concrete workflow. Extract reusable transitions, assignments and versioning only after repeated patterns are proven. Sequential approval, parallel review, reassignment, delegation, recusal, deadlines and escalation each require explicit tests; HRMPSB deliberation remains a separate policy-validated design. A configurable engine is not authorized merely because common patterns appear.

Commands request actions; domain events describe completed facts using past-tense names and stable identifiers. Events minimize sensitive payloads. Listeners/jobs are idempotent, retries and terminal failures are observable, and correlation IDs join domain/audit/integration evidence. Notifications remain delivery records and cannot reverse or become business truth.

For each concrete workflow, approve owning aggregate, domain status versus workflow state, authorized transitions, assignment/authority, office scope, applicable versions/snapshots, deadlines/calendar, evidence/documents, events, audit fields, notification rules, concurrency behavior, failure recovery and acceptance tests.

