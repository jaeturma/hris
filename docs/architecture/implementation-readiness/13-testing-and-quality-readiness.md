# Testing and Quality Readiness

## Initial quality gate

Phase 1 work must pass the narrow relevant tests first and then the approved pipeline: Pest/PHPUnit, Larastan/PHPStan, Pint, frontend TypeScript, ESLint/Prettier checks and production Vite build. WP-1 must verify actual script names and versions rather than trusting documentation.

No work package is accepted with an unauthorized route, missing Policy for a sensitive action, broken office scope, untested critical permission, sensitive serialization leak, destructive/unreviewed migration, failing check, or critical/high defect.

## Testing readiness matrix

| Layer | Phase 1 use | Minimum evidence |
|---|---|---|
| Unit/domain | identifiers, scope rules, value objects where justified | boundaries and edge cases |
| Feature/database | routes, validation, persistence, constraints | allowed and invalid paths |
| Policy/authorization | every protected action | role + Policy + scope + assignment matrix |
| Data-scope | hierarchy/context queries | same-office, cross-office, oversight, inactive assignment |
| Workflow/event/queue | only when introduced | transitions, idempotency, retry/failure |
| Notification | when introduced | content minimization and delivery independence |
| Browser | critical shell/office-switch path | navigation, JS errors and user-visible state |
| Accessibility | shell/components | keyboard, focus, semantics, contrast, error announcement |
| Security | routes, mass assignment/serialization, exports/files | negative cases and headers/session review |
| Performance | hierarchy/scope queries | query count and agreed volume budget |
| Migration/seeder | every schema/reference change | forward/rollback expectation, idempotency and rerun safety |

## Synthetic test data

Factories/scenarios must use fictional employees/applicants across Region, Division, District, School and IU scopes; multiple roles, expired/delegated authority, sensitive/restricted records, history/effective dates, policy versions and workflow assignments. Never use production personnel/applicant data.

**Assessment: Amber.** Strategy is adequate; WP-1 must establish a passing baseline and CI-equivalent commands (C-07).

