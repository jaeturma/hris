# Phase 1 Definition of Done

| Area | Required evidence |
|---|---|
| Functional | specified outcome and error behavior exist; testable criteria pass |
| Architecture | domain/write ownership respected; no shortcut/cross-domain write; references/ADRs current |
| Database | separately approved migrations; justified constraints/indexes; history/effective dates; safe rollback/forward repair; idempotent seeders |
| Security | server authorization/scope; no admin overreach/secrets/leaks; sensitive actions audited; negative tests |
| Backend | server validation; thin controllers; simplest justified actions/services; transactions/error handling |
| Frontend | typed props; visible errors/loading/empty/failure; responsive/accessibility; UI not authorization |
| Testing/tooling | relevant automated tests, auth/scope/regression/migration/seeder checks; Pest/PHPUnit, PHPStan, Pint, types/lint/build pass as configured |
| Documentation | architecture/entity/permission/audit/seeder/route/dev/user/traceability/changelog/progress updated as applicable |
| Review | code, QA, security/privacy/data/business/policy review as selected; no Critical/blocking High defect |
| Evidence | commit/PR, files, commands/results, screenshots where UI, approvals, limitations/debt and status recorded |

All items are mandatory when applicable. “Not applicable” requires rationale and reviewer acceptance.
