# ADR-001 Policy Rules Are Versioned and Configurable

## Status

Accepted

## Decision

Policy-driven rules must be versioned and configurable through the Policy and Configuration Domain instead of hardcoded into controllers, React components, or model methods.

## Rationale

DepEd Orders, Memoranda, CSC rules, MSPs, assessment frameworks, and local implementing issuances change over time. Core code should not be rewritten for every policy change.

## Consequences

Phase 1 must include policy registry, policy versioning, source storage, approval workflow, and audit before policy-driven modules.
