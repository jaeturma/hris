# Definition of Done

| DoD area | Required evidence |
|---|---|
| Scope/architecture | approved work package implemented; exclusions preserved; domain owner/boundary and ADRs respected |
| Data | reviewed logical/physical design, constraints/indexes/history and migration/rollback evidence where applicable |
| Validation/security | Form Request/input validation; permission + Policy + office scope + assignment/SoD; restricted data protected |
| Audit/events/errors | approved audit fields and relevant past-tense events; idempotency/error/failure handling |
| Tests | functional, validation, authorization, cross-office/scope, history/audit and relevant frontend/migration/seeder tests pass |
| Quality | PHP tests/static analysis/Pint and frontend type/lint/format/build checks pass |
| UX | responsive/accessibility states and destructive/restricted warnings reviewed |
| Documentation | architecture, ADR, traceability, API/user/release docs updated as applicable |
| Defects/review | no critical/high unresolved defect; technical/security/privacy/HR/human reviews completed as required |
| Policy-sensitive | governing source/provision/version/applicability confirmed; configuration and expected result validated by Policy and HR Process Owners |

A work package is not Done when code exists but tests, human review, traceability or acceptance evidence are missing. Deferred work and known limitations are recorded and cannot conceal failed acceptance criteria.

