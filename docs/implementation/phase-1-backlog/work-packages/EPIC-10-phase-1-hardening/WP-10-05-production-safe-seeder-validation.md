# WP-10-05 — Production-Safe Seeder Validation

| Field | Value |
|---|---|
| ID / Epic | WP-10-05 / EPIC-10 Integration, Hardening and Phase Acceptance |
| Status / Priority | Blocked / P1 |
| Domain / Reviewer | Cross-cutting Governance / Architect, QA, Security and Business Acceptance |
| Risk / Complexity | High / Medium |

## Objective, context and scope

Produce independently reviewable production-safe seeder validation evidence for Phase 1 acceptance. It must preserve server-enforced office/authority controls and Phase 0.13 acceptance splits.

Include only Production-Safe Seeder Validation, focused tests/review evidence and documentation. Exclude new HR modules, generic page builders, auth redesign, speculative components, AI/analytics, production deployment and unrelated fixes. Dependencies: All relevant Phase 1 mandatory packages substantially Accepted; preceding EPIC-10 evidence package.

## References and policy

Phase 0.12 hardening/release/DoD; Phase 0.13 G-009; Phase 1 gates and DoD; security/UI/testing standards, permission/audit catalogs and DoD. No direct HR policy rule is implemented. Accessibility, privacy, records and government audit controls apply; do not invent provisions.

## Database/backend/frontend

No new business schema. Review approved migration/seeder order, reversibility/forward repair, history and idempotency using existing artifacts; do not execute destructive or unapproved operations.

Backend changes are limited to approved typed props/queries or correction of an explicitly accepted hardening defect. Controllers remain thin; Policies and server scope remain authoritative.

Frontend: No feature UI; review existing behavior/evidence only.

## Permissions, scope, audit and events

Do not introduce generic permissions. Use approved abilities and Policies. Wrong-office, stale context, expired authority and technical-admin-without-business-authority are denied. Preserve them and report any gap.

Audit any approved correction and record review evidence/correlation. No new domain event unless an approved correction creates a real completed fact with consumer.

## Validation/security/tests

Validate props/URLs/input server-side, prevent sensitive serialization and scope inference, preserve CSRF/session/security headers, and expose no secrets. Test or review focused behavior plus authorization/scope negatives, regression, TypeScript/static/lint/build, accessibility, migration/seeder/audit evidence as applicable. Manual review supplements, never replaces practical automation.

## Acceptance criteria

- Production-Safe Seeder Validation has objective evidence mapped to exact packages/requirements and no hidden dependency.
- Unauthorized/wrong-office/stale/expired behavior remains denied; frontend cannot bypass server control.
- Applicable automated/regression/security evidence passes.
- Any Critical/High defect blocks acceptance and receives an owner/remediation package.
- Documentation/traceability/status/evidence are complete; no unrelated feature is added.

Apply central DoD. Evidence includes files/commits, commands/results, matrices, screenshots where UI, findings/disposition, approvals, limitations and final status.

## Ready-to-Paste Codex Instruction

> Execute WP-10-05 — Production-Safe Seeder Validation only after All relevant Phase 1 mandatory packages substantially Accepted; preceding EPIC-10 evidence package. Read AGENTS.md, Phase 0.12 hardening/release/DoD; Phase 0.13 G-009; Phase 1 gates and DoD, Phase 0.13 gaps, catalogs/gates/DoD and this package; inspect code/Git first.
>
> Perform only Production-Safe Seeder Validation. Generate evidence and only approved corrective changes. Do not run unapproved/destructive migrations or seeders. Add/run focused automated negative and regression checks.
>
> Do not install packages, change auth, add business modules, waive High defects, treat UI as authorization, invent policy or refactor unrelated work. Stop on conflict. Report files, commands/tests/results, findings, corrections, documentation, approvals and unresolved issues.

