# Ready-to-Paste Phase 1 Kickoff Instruction

Copy only after the Phase 1 entry conditions and explicit WP-1 development approval are recorded.

---

# Phase 1, Work Package 1 — Foundation Baseline Verification

## Objective

Establish a factual, reproducible baseline for the existing **HRIS for DepEd** Laravel 13 + React + Inertia repository and determine readiness for WP-2. Do not implement organization hierarchy or any HRIS module.

## Required reading

Read `AGENTS.md`; all relevant `.codex/*.md`; `docs/project-standards/`; architecture blueprint, data, security, UI, domains, events/workflows, documents/records, policy/AI/analytics, decisions, implementation-readiness; and `docs/implementation/`. Treat Phase 0.11 Conditional GO and the Phase 1 exclusions as controlling.

## Existing-state inspection

Before editing, inspect Git status without altering user changes. Identify:

- PHP, Laravel, Composer, Node/npm, React, Inertia, TypeScript and database-driver versions.
- Installed Composer and npm packages, especially Fortify/auth, Spatie Permission/Activitylog, Pest/PHPUnit, Larastan/PHPStan, Pint, ESLint, Prettier, Vite, Tailwind and Wayfinder.
- Current routes and middleware without exposing sensitive values.
- Existing login, registration, password reset, verification, profile/security and logout behavior. Do not modify authentication.
- Laravel directories, configuration, migrations and providers.
- React/Inertia pages, layouts, components, types, route helpers and build configuration.
- Test suites, factories and documented scripts.
- Database connection type/configuration names while redacting hosts, users, passwords, tokens and secrets.
- Existing warnings, failing checks, uncommitted/overlapping work and architecture deviations.

## Verification

Confirm the real script definitions before running them. Run the narrowest non-destructive checks, then where configured and safe:

- Laravel/Pest/PHPUnit tests.
- Pint formatting check without rewriting files.
- Larastan/PHPStan.
- TypeScript type checking.
- ESLint and Prettier checks without rewriting files.
- Production frontend build.

Do not migrate, seed, reset, refresh, import data, modify the database, install/update packages, change environment secrets, clear shared data, or run destructive commands. Do not expose `.env` contents or credentials.

## Scope

Produce a baseline report and evidence only. A minimal documentation-only correction is allowed when clearly required to make the report accurate. Any code/configuration correction requires explicit scope and approval before editing.

## Out of scope / prohibited changes

No migrations, models, controllers, requests, services/actions, Policies, jobs/events/listeners/notifications, routes, React pages/components, seeders, organization data, office scope, permission changes, workflow/policy engines, documents, integrations, analytics or AI. Avoid unrelated refactoring and package installation.

## Required report

Provide:

1. Current environment summary.
2. Composer/npm package and version summary.
3. Current backend and frontend code structure.
4. Route/middleware and authentication behavior summary.
5. Database configuration summary with secrets redacted.
6. Current tests and exact results.
7. Pint and static-analysis status.
8. TypeScript, lint/format and frontend-build status.
9. Existing warnings/errors and whether pre-existing.
10. Git/worktree risks and files changed, if any.
11. Recommended corrective actions, owners and blocking effect.
12. A final **GO**, **CONDITIONAL GO**, or **NO-GO** recommendation for WP-2.

Stop and report rather than inventing policy, changing auth, installing packages, modifying production code outside scope, or resolving unrelated user changes.

---

