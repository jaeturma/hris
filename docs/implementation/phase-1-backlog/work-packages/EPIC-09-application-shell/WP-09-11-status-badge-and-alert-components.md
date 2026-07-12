# WP-09-11 — Status Badge and Alert Components

| Field | Value |
|---|---|
| ID / Epic | WP-09-11 / EPIC-09 Application Shell and UI Foundation |
| Status / Priority | Blocked / P1 |
| Domain / Reviewer | Core Platform UI / UI/UX, Accessibility and Security Reviewers |
| Risk / Complexity | Medium / Medium |

## Objective, context and scope

Deliver a reusable, accessible status badge and alert components outcome without creating business-module pages. It must preserve server-enforced office/authority controls and Phase 0.13 acceptance splits.

Include only Status Badge and Alert Components, focused tests/review evidence and documentation. Exclude new HR modules, generic page builders, auth redesign, speculative components, AI/analytics, production deployment and unrelated fixes. Dependencies: Accepted WP-01 baseline; shared UI conventions; office-context parts wait for EPIC-04, permission navigation for EPIC-05; preceding EPIC-09 WP.

## References and policy

application-shell.md; design-system.md; accessibility.md; .codex/ui.md; ADR-017; Phase 0.13 G-014; security/UI/testing standards, permission/audit catalogs and DoD. No direct HR policy rule is implemented. Accessibility, privacy, records and government audit controls apply; do not invent provisions.

## Database/backend/frontend

No database changes.

Backend changes are limited to approved typed props/queries or correction of an explicitly accepted hardening defect. Controllers remain thin; Policies and server scope remain authoritative.

Frontend: use TypeScript/Inertia and existing Tailwind/design conventions; explicit minimal props; keyboard/focus/semantic labels/contrast; responsive loading/empty/error/denied states; visible office/acting/restricted/draft-final context; permission-aware controls never authorize.

## Permissions, scope, audit and events

Do not introduce generic permissions. Use approved abilities and Policies. Wrong-office, stale context, expired authority and technical-admin-without-business-authority are denied. Preserve them and report any gap.

Audit any approved correction and record review evidence/correlation. No new domain event unless an approved correction creates a real completed fact with consumer.

## Validation/security/tests

Validate props/URLs/input server-side, prevent sensitive serialization and scope inference, preserve CSRF/session/security headers, and expose no secrets. Test or review focused behavior plus authorization/scope negatives, regression, TypeScript/static/lint/build, accessibility, migration/seeder/audit evidence as applicable. Manual review supplements, never replaces practical automation.

## Acceptance criteria

- Status Badge and Alert Components has objective evidence mapped to exact packages/requirements and no hidden dependency.
- Unauthorized/wrong-office/stale/expired behavior remains denied; frontend cannot bypass server control.
- Keyboard, focus, semantic, responsive and state requirements pass.
- Any Critical/High defect blocks acceptance and receives an owner/remediation package.
- Documentation/traceability/status/evidence are complete; no unrelated feature is added.

Apply central DoD. Evidence includes files/commits, commands/results, matrices, screenshots where UI, findings/disposition, approvals, limitations and final status.

## Ready-to-Paste Codex Instruction

> Execute WP-09-11 — Status Badge and Alert Components only after Accepted WP-01 baseline; shared UI conventions; office-context parts wait for EPIC-04, permission navigation for EPIC-05; preceding EPIC-09 WP. Read AGENTS.md, application-shell.md; design-system.md; accessibility.md; .codex/ui.md; ADR-017; Phase 0.13 G-014, Phase 0.13 gaps, catalogs/gates/DoD and this package; inspect code/Git first.
>
> Perform only Status Badge and Alert Components. Use typed accessible Inertia/React and preserve server-authorized office/permission context.  Add/run focused automated negative and regression checks.
>
> Do not install packages, change auth, add business modules, waive High defects, treat UI as authorization, invent policy or refactor unrelated work. Stop on conflict. Report files, commands/tests/results, findings, corrections, documentation, approvals and unresolved issues.

