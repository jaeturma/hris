# Testing, Quality, and Observability Gap Review

## Coverage gaps

| Area | Planned coverage | Gap / condition |
|---|---|---|
| unit/feature/domain/database | Phase 0.12 quality matrix | WP-1 must verify actual tools/scripts; domain invariants defined per WP |
| authorization/office scope | strong negative matrix | add restructuring, stale context, expired authority, recusal and archival access |
| workflow/event/queue/notification | idempotency/failure planned | add suspension/reopen/concurrency/dead-letter recovery cases |
| migration/seeder/import | constraints/idempotency/reconciliation planned | define lock/volume/partial-failure and forward-repair tests |
| browser/accessibility | shell checks planned | approve browsers, assistive-tech/manual protocol and critical flows |
| security/performance | named layers | threat scenarios and quantitative budgets absent |
| policy versions | snapshot tests planned | transition/retroactive/conflict/active-case cases missing |

## Observability gaps

Failed jobs/notifications, policy conflicts, authorization denials, restricted access/exports, integration/data-quality/migration/signature failures and future AI incidents require event names, severity, correlation, redaction, owner, alert threshold, response runbook, retention and closure evidence. Phase 0.12 names monitoring but does not define this operational catalog.

Pest, PHPUnit, Pint, Larastan/PHPStan, TypeScript, ESLint/Prettier and build remain unverified until WP-1. Quality gates are structurally sound but observability and performance gates are too qualitative for production.

