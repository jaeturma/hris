# ADR-017: Foundation First and Server-Enforced Office Scope

- Status: Accepted in Phase 0.11, subject to Phase 1 approval
- Date: 2026-07-12

## Context

All sensitive HR domains depend on a trustworthy DepEd organization hierarchy, user-office authority, active context, authorization and audit. UI filtering alone cannot enforce isolation.

## Decision

Phase 1 is foundation-only. Organization and office scope precede business modules. Every sensitive request is scoped server-side and evaluated through permission, Laravel Policy, office/ancestry context and applicable assignment/authority checks. Technical administration supplies no implicit HR approval authority.

## Consequences

Business modules remain excluded until scope and authority tests pass. Scope contracts become shared foundation dependencies and require strict change control.

