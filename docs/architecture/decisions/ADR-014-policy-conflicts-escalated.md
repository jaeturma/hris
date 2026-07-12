# ADR-014 Policy Conflicts Are Escalated, Not Silently Resolved

## Status

Accepted

## Decision

When policies conflict or applicability is unclear, the system creates a controlled review task for authorized HR/legal policy review.

## Rationale

The system must not guess policy interpretation for high-impact HR actions.

## Consequences

Policy resolution snapshots must include conflicts, reviewer decision, basis, and transition handling.
