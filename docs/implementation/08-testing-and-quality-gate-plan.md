# Testing and Quality Gate Plan

## Quality gates

| Gate | Evidence | Blocking rule |
|---|---|---|
| Baseline | verified PHP/Composer/Node packages, auth/routes, test and script inventory | WP-2 cannot start without WP-1 recommendation |
| Focused development | narrow Pest tests, relevant frontend checks | no failing relevant check |
| Authorization/security | Policy, office-scope, assignment, negative tests | any scope leak or unauthorized route blocks |
| Data/migration | constraints, migration behavior, seeder idempotency, synthetic data | no unreviewed destructive migration |
| Integrated backend | full approved Pest/Composer test pipeline and PHPStan/Larastan | all pass; no unjustified suppression |
| Integrated frontend | TypeScript, ESLint, Prettier and production build | all pass |
| UX/accessibility | keyboard/focus/semantics/errors/contrast/responsive review | critical accessibility flow defects block |
| Acceptance | regression, traceability, no critical/high open defect, human review | required sign-offs recorded |

Commands currently documented are `php artisan test --compact`, `composer test`, `composer types:check`, `composer lint`, `npm run lint:check`, `npm run format:check`, `npm run types:check`, and `npm run build`; WP-1 must verify them before they become controlling evidence.

Testing layers include unit/domain, feature/database, validation, Policy/authorization, data scope, workflow/event/queue/notification, integration adapters, browser, accessibility, security, performance, migration and seeder tests. Use fictional multi-office, historical, permission, policy-version and restricted-data scenarios only.

Quality exceptions require written reason, owner, risk, expiry and approval; they cannot waive critical security, authorization, integrity or policy tests.

