# Coding Standards

These rules apply to future implementation work in this Laravel 13 + React + Inertia HRIS.

## General

- Follow existing code style before introducing new patterns.
- Keep changes focused on the requested behavior.
- Do not edit Laravel core, vendor files, or generated framework internals.
- Do not change authentication flow unless explicitly requested.
- Do not install packages without approval.
- Prefer clear names based on DepEd HR language.

## Laravel

- Use Laravel conventions for controllers, models, policies, Form Requests, migrations, seeders, jobs, events, and notifications.
- Keep controllers thin. Validation belongs in Form Requests; complex business behavior belongs in actions or services.
- Use Eloquent relationships, scopes, casts, accessors, and mutators deliberately and consistently.
- Use authorization checks for every sensitive action.
- Use database transactions for multi-step personnel actions.
- Use events or activity logging for auditable state changes.
- Avoid raw SQL unless it is justified by performance and covered by tests.

## React and Inertia

- Use TypeScript for React components and pages.
- Use Inertia forms and navigation patterns already present in the starter kit.
- Use Wayfinder-generated route helpers when connecting React pages to Laravel routes.
- Keep page props explicit and typed.
- Keep UI state local unless shared state is clearly required.
- Avoid duplicating authorization logic in the browser. Frontend checks may hide controls, but Laravel must enforce permissions.

## Naming

- Use domain names such as `Employee`, `PlantillaItem`, `PositionTitle`, `SalaryGrade`, `Appointment`, `ServiceRecord`, `LeaveApplication`, and `PerformanceRating`.
- Use office scope names such as `Region`, `Division`, `District`, `School`, and `ImplementingUnit`.
- Name permissions as actions on domain resources, for example `employees.view`, `appointments.approve`, or `service-records.export`.

## Formatting and Static Analysis

- Format PHP with Laravel Pint.
- Format frontend code with Prettier.
- Keep TypeScript, ESLint, and PHPStan/Larastan clean.
- Do not silence static analysis unless the reason is documented and narrow.

## Comments

Use comments only for non-obvious domain or policy decisions. Avoid comments that restate the code.
