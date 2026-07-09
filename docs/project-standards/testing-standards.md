# Testing Standards

Testing uses Pest 4 and must protect government HR behavior.

## Test Types

- Feature tests: routes, Inertia responses, validation, authorization, workflows, and audit logging.
- Unit tests: isolated services, actions, value objects, enums, and business rules.
- Authorization tests: role, permission, policy, and office-scope access.
- Validation tests: required fields, formats, dates, statuses, and policy-aware constraints.
- Business rule tests: appointments, promotions, transfers, leave, service records, plantilla rules, and HRMPSB flows when implemented.
- Browser tests: only for important end-to-end UI flows or JavaScript risk.

## Naming

- Test files should describe the behavior, for example `AppointmentApprovalTest`.
- Pest test descriptions should read like behavior statements.
- Use datasets for repeated validation cases.

## Coverage Expectations

Every future module should test:

- Allowed user can perform the action.
- Unauthorized user is forbidden.
- Office scope is enforced.
- Invalid data is rejected.
- Official history is preserved.
- Activitylog entry is created where required.
- Sensitive exports are permission-gated.
- Inertia pages receive expected props.

## Commands

- Narrow test: `php artisan test --compact --filter=Name`
- Test file: `php artisan test --compact tests/Feature/ExampleTest.php`
- Full PHP test suite: `php artisan test --compact`
- Full Composer test pipeline: `composer test`
- Static analysis: `composer types:check`
- PHP formatting: `composer lint`
- Frontend checks: `npm run lint:check`, `npm run format:check`, `npm run types:check`, `npm run build`

Do not remove tests without explicit approval.
