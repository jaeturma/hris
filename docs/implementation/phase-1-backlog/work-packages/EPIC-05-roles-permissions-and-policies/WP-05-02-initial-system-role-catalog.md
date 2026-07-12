# WP-05-02 — Initial System Role Catalog

| Field | Value |
|---|---|
| ID / Epic | WP-05-02 / EPIC-05 Roles, Permissions and Authorization Policies |
| Status / Priority | Blocked / P0 |
| Domain / Reviewer | Core Platform/Governance / Security Reviewer and HR Process Owner |
| Risk / Complexity | High / Medium |

## Objective, context and scope

Establish the independently testable initial system role catalog capability within Roles, Permissions and Authorization Policies. This protects DepEd multi-office records and separates technical capability from HR business authority. Include only Initial System Role Catalog, its focused tests and documentation. Exclude business modules, generic engines, unrelated auth/UI changes, production data and deployment.

Dependencies: Accepted EPIC-04 scope contract and bootstrap audit; C-05/C-06; preceding EPIC-05 WP. Predecessors must be Accepted.

## References and policy

role-catalog.md; permission-matrix.md; approval-authority.md; ADR-011/012/017; Phase 0.13 G-005/G-006; Phase 1 permission/audit catalogs, governance and DoD. No substantive HR policy is implemented. Privacy, audit and records controls apply; authority meaning requires approved HR/Security review.

## Database, backend and frontend

No database change assumed; any persistence discovered requires DB/architecture approval.

Backend uses scoped queries, explicit services only for non-trivial scope/authority logic, Laravel Policies, Form Requests, thin controllers, transactions and denial-safe errors. Never use role names as primary authorization.

Frontend: No frontend changes unless the approved package explicitly needs them.

## Permission, office scope and audit

Apply the exact Phase 1 permission catalog. Require permission + Policy + authorized active office/ancestry + assignment/valid delegation + SoD. Regional oversight is not global management; administrators have no implicit HR authority.

Audit successful and security-relevant actions with actor, role/capacity, office, subject, old/new, reason, authority/basis and correlation. Access to restricted audit is itself audited. Domain events require a real idempotent consumer; audit is not an event substitute.

## Validation/security/tests

Validate validity dates, non-overlap, ancestry, active status, revocation, conflicts and immutable prior evidence. Deny cross-office, stale context, inactive assignment, expired delegation, recusal and privilege escalation. Test unit scope/authority logic; feature/Policy/database behavior; same/cross/oversight cases; technical-admin denial; audit completeness/redaction; frontend/build/accessibility if applicable; regression.

## Acceptance criteria and evidence

- Authorized in-scope behavior succeeds; unauthorized, wrong-office, stale or expired authority receives 403/no disclosure.
- Privileged mutations cannot occur before bootstrap audit and produce attributable evidence.
- History/revocation and SoD rules remain intact.
- Focused and applicable quality checks pass; architecture/docs/catalogs/traceability update.
- Completion evidence lists files, commits, commands/results, security review, limitations and status.

Apply central DoD. Stop on unresolved C-05/C-06, scope, authority, privacy or records conflict.

## Ready-to-Paste Codex Instruction

> Execute WP-05-02 — Initial System Role Catalog only after Accepted EPIC-04 scope contract and bootstrap audit; C-05/C-06; preceding EPIC-05 WP. Read AGENTS.md, security/domain/audit references, Phase 0.13 gaps, this package and DoD; inspect existing code/Git first.
>
> Implement only Initial System Role Catalog. No database change assumed; any persistence discovered requires DB/architecture approval. No frontend changes unless the approved package explicitly needs them. Enforce server-side Laravel Policies and office/authority scope, Form Request validation, thin controllers, bootstrap/full audit as applicable and automated negative tests.
>
> Do not install packages, alter auth, add business modules, invent authority/policy, migrate/seed without approval, trust frontend checks or refactor unrelated work. Stop for human resolution on conflict. Report files, DB impact, tests/commands/results, audit/security evidence, docs and unresolved issues.

