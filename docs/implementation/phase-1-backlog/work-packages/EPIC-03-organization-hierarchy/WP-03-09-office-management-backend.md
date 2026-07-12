# WP-03-09 — Office Management Backend

| Field | Value |
|---|---|
| ID / Epic | WP-03-09 / EPIC-03 Organization Hierarchy |
| Status / Priority / Wave | Blocked / P1 / Phase 1 |
| Domain / Reviewer | Organization / Organization Owner, Architect and Database Reviewer |
| Risk / Complexity | Medium / Medium |

## Objective and context

Deliver an independently reviewable office management backend outcome for Organization Hierarchy without expanding into later HRIS domains. It applies foundation-first, server-scoped and history-preserving decisions required by future DepEd modules.

## Scope, exclusions and dependencies

Include only inspection and the named Office Management Backend concern, focused tests and documentation. Exclude unrelated refactoring, packages, auth redesign, later epics, HR business modules, production data/deployment and generic engines.

Dependencies: Accepted EPIC-01/02; C-02, C-03, C-04; preceding EPIC-03 package; immediate predecessors must be Accepted. Phase 0.13 gaps require approved evidence.

## Architecture and policy references

office-hierarchy.md; organization-structure.md; organization-domain.md; ADR-017; Phase 0.13 G-003/G-008; backlog governance and Phase 1 DoD. No direct policy rule is implemented unless a verified source is attached. Privacy, records/audit and official reference provenance remain control context; invent no provisions.

## Database, backend and frontend

No database changes assumed; stop for approval if persistence is discovered.

Backend: inspect first; use simplest Laravel patterns, Form Requests for request validation, thin controllers, transactions for multi-record writes, scoped queries and explicit errors. No role-name business decisions or cross-domain writes.

Frontend: No frontend changes unless explicitly approved.

## Authorization, scope, audit and events

No new permission by default; stop if protected state lacks a defined Policy. System-wide/national scope must be explicit. School users cannot manage other schools; oversight requires permission and ancestry authority; stale/inactive context is denied.

Audit material actions with actor, role/capacity, office, entity, old/new where applicable, reason/basis, correlation and redaction. No domain event unless a legitimate consumer needs a completed fact.

## Validation, security, tests and documentation

Validate required formats, uniqueness, parent/effective/status/conflict/archive rules server-side. Require auth, CSRF/session, mass-assignment/serialization controls, safe public IDs and no secrets. Test unit/feature behavior, authorization/wrong-office/expired authority negatives, DB/seeder behavior and frontend/type/build/accessibility as applicable, plus auth/starter regression.

Update affected architecture/entity/permission/audit/seeder/route/developer/user docs, traceability, changelog and status.

## Acceptance criteria

- The named outcome is demonstrable with accepted dependencies and no unrelated behavior change.
- Unauthorized, wrong-office, stale-context or expired-authority access is denied server-side with no disclosure/mutation.
- Material changes preserve required history and attributable audit evidence.
- Focused tests and applicable static/type/lint/build checks pass.
- Architecture or policy conflict stops work for human resolution.

## DoD, risks and evidence

Apply central DoD. Mitigate scope drift, weak negatives and unresolved data/authority decisions using stop gates. Record files/commits, commands/results, schema/rollback review, UI evidence, docs, approvals, limitations and status.

## Ready-to-Paste Codex Instruction

> Task: WP-03-09 — Office Management Backend. Read AGENTS.md, relevant .codex rules, office-hierarchy.md; organization-structure.md; organization-domain.md; ADR-017; Phase 0.13 G-003/G-008, Phase 0.13 gaps, governance, this package and DoD. Inspect code and Git status first; preserve user changes.
>
> Deliver only Office Management Backend. Dependencies: Accepted EPIC-01/02; C-02, C-03, C-04; preceding EPIC-03 package. No database changes assumed; stop for approval if persistence is discovered. No frontend changes unless explicitly approved.
>
> Enforce server validation, Laravel Policies and office scope; use Form Requests, thin controllers, audit, focused negative tests and verified quality checks. Do not install packages, redesign auth, add later modules, invent policy, expose secrets, migrate/seed without approval or refactor unrelated files.
>
> Stop for human decision on conflicts. Report files, database impact, commands/tests/results, acceptance evidence, docs and unresolved issues.

