# ADR-019: Effective-Dated History and Idempotent Reference Seeding

- Status: Accepted in Phase 0.11
- Date: 2026-07-12

## Context

Government HR records and official reference values change over time, while completed decisions must remain reproducible.

## Decision

Historical HR assignments/actions and versioned official configuration use append/supersession or effective-dated structures rather than destructive overwrite. Production reference seeders are source-traceable, deterministic, idempotent, non-destructive and safe to rerun. Office and policy scoping are tested before affected modules are accepted.

## Consequences

Schema reviews must address temporal uniqueness and correction semantics. Seed-data changes require source/version review and tests.
