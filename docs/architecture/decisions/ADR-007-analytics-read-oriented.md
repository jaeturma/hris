# ADR-007 Analytics Are Read-Oriented

## Status

Accepted

## Decision

Analytics, dashboards, and reports may read across domains but cannot modify operational records.

## Rationale

Reporting should not own source records or business decisions.

## Consequences

Corrections must be routed to owning domains. Report snapshots and exports are audited.
