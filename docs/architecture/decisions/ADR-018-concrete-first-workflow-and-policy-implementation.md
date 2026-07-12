# ADR-018: Concrete-First Workflow and Policy Implementation

- Status: Accepted in Phase 0.11
- Date: 2026-07-12

## Context

DepEd processes share patterns but differ in authority, policy, evidence and legal effect. An unrestricted generic engine before validated cases would hide differences and increase coupling.

## Decision

Implement a minimal versioned policy registry in Phase 1. Implement workflow and policy behavior incrementally for approved concrete cases, then extract only repeated, tested primitives. Do not implement a universal workflow designer or generic rules language in Phase 1.

## Consequences

Some duplication may temporarily remain visible. Policy/workflow versions and transaction snapshots are mandatory when policy-sensitive modules begin.

