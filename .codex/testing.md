# Testing and Verification Rules

Testing for this project uses Pest 4. Static analysis uses Larastan/PHPStan. Formatting uses Laravel Pint, Prettier, and ESLint.

## Required Mindset

Tests must protect government HR workflows, not just happy paths. Every future module should include coverage for authorization, validation, office scoping, audit logging, and important state transitions.

## Pest 4

- Write tests in Pest syntax.
- Use Feature tests for routes, Inertia responses, authorization, validation, and workflow behavior.
- Use Unit tests for isolated services, actions, value objects, and policy helpers.
- Use Browser tests only when end-to-end UI behavior or JavaScript risk warrants it.
- Do not delete tests without explicit approval.

## What to Test

For each module, test authorized users, unauthorized users, office scoping, validation, historical preservation, Activitylog entries, export permissions, reports, and Inertia props.

## Commands

- `php artisan test --compact --filter=Name`
- `php artisan test --compact tests/Feature/SomeTest.php`
- `php artisan test --compact`
- `composer lint`
- `composer types:check`
- `composer test`
- `npm run lint:check`
- `npm run format:check`
- `npm run types:check`
- `npm run build`

## Static Analysis

- Keep Larastan/PHPStan clean.
- Prefer typed method signatures and explicit return types where consistent with the codebase.
- Do not suppress analysis unless the suppression is narrow and justified.

## Frontend Verification

- Type-check React and Inertia code.
- Build with Vite before finishing significant UI work.
- Confirm no JavaScript console errors when browser testing is used.

## Test Data

Use factories and seeders that reflect DepEd structures. Test data should include Region, Division, District, School, Implementing Unit, Plantilla Item, Position Title, Salary Grade, Item Number, and Employee relationships where relevant.
