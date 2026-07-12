# ADR-003 Active Transactions Preserve Policy Snapshots

## Status

Accepted

## Decision

Active and completed transactions preserve the exact policy, rule, workflow, document checklist, template, QS, assessment, and competency versions used.

## Rationale

Later policy changes must not silently alter evaluations, appointments, career decisions, or records.

## Consequences

Workflow instances require configuration snapshots and transition handling for superseded policies.
