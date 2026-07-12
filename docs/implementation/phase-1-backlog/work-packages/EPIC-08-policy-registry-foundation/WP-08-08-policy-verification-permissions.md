# WP-08-08 — Policy Verification Permissions

| Field | Value |
|---|---|
| ID / Epic | WP-08-08 / EPIC-08 Policy Registry Foundation |
| Status / Priority | Blocked / P0 |
| Domain / Reviewer | Policy and Configuration / Policy Validator, HR Owner and Security Reviewer |
| Risk / Complexity | High / Medium |

## Objective and context

Deliver a reviewable policy verification permissions outcome for Policy Registry Foundation, preserving authoritative provenance, effective versions and human accountability. This is foundation configuration, not employee transactions, scoring, Rules Engine or policy interpretation.

## Scope, exclusions and dependencies

Include only Policy Verification Permissions, focused backend/frontend work when named, automated tests and documentation. Exclude unverified national values, destructive updates, generic rules/workflows, source-file storage beyond approved metadata, business modules, AI and production import.

Dependencies: Accepted relevant EPIC-05/06/07 packages; verified minimum registry scope; preceding EPIC-08 WP; predecessors must be Accepted.

## References and policy

policy registry/versioning architecture; ADR-001/002/003/014/018; Phase 0.13 G-011; reference/permission/audit catalogs and DoD. Only verified issuance metadata may be represented. Do not encode a substantive rule, precedence, retroactivity or applicability without signed Policy/HR validation.

## Database/backend/frontend

No database changes unless approved after inspection.

Backend uses explicit validation, Laravel Policies, scoped queries, thin controllers and transactional lifecycle changes. National, system and office-managed stewardship remain distinct. Policy registration, verification, approval and activation are segregated.

Frontend: No frontend changes unless explicitly required.

## Authorization, scope, audit and events

Use exact reference/policy permissions and record Policies; maker-checker/SoD and business authority apply. Administrators cannot self-verify or activate without separate authority. Audit old/new, source/version, status/effective date, reason, actor/capacity/office and correlation. Emit a past-tense event only for a genuine consumer; listeners must be idempotent and payload-minimal.

## Validation, security and tests

Require source/provenance, code/title, allowed lifecycle, temporal consistency, no cycles, scoped uniqueness, immutable used versions and non-destructive supersession. Deny wrong steward/office, invalid transition, duplicate seed, unauthorized activation and restricted-source leakage. Test units, features, Policies/scope, constraints/effective dates, seed reruns, audit, frontend types/accessibility/build and regression as applicable.

## Acceptance and evidence

- Valid authorized records/transitions persist with source, version/history and attributable audit.
- Invalid dates/status/cycles/duplicates and unauthorized/wrong-scope actions fail without mutation.
- Production-safe seeds are deterministic, idempotent and never overwrite official used history.
- No substantive policy rule or generic engine is introduced.
- Quality checks/docs/traceability pass and evidence records files, commands/results, approvals, limitations and status.

Apply central DoD; stop for missing source, policy meaning, C-04 or authority decision.

## Ready-to-Paste Codex Instruction

> Execute WP-08-08 — Policy Verification Permissions only after Accepted relevant EPIC-05/06/07 packages; verified minimum registry scope; preceding EPIC-08 WP. Read AGENTS.md, policy registry/versioning architecture; ADR-001/002/003/014/018; Phase 0.13 G-011, Phase 0.13 gaps, catalogs, this package and DoD; inspect existing code/Git first.
>
> Implement only Policy Verification Permissions. No database changes unless approved after inspection. Use Form Requests, thin controllers, Policies, server office/steward scope, version/history-safe writes, audit and focused negative/idempotency tests. No frontend work.
>
> Do not invent policy/reference values, build Rules Engine, install packages, migrate/seed without approval, overwrite history or refactor unrelated work. Stop on policy/architecture conflict. Report files, DB impact, tests/commands/results, approvals, documentation and unresolved issues.

