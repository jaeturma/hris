# Coding Standards

These standards apply to future Laravel, React, and Inertia code.

## Laravel Rules

- Keep controllers thin.
- Put validation in Form Requests.
- Put authorization in policies, gates, or Spatie permissions.
- Put multi-step business logic in services or actions.
- Use dependency injection instead of service locator calls when practical.
- Use constructor property promotion where it improves readability.
- Use typed properties, parameters, and return types.
- Use enums for stable state sets.
- Avoid duplicate logic.
- Avoid magic numbers and unexplained policy constants.
- Keep functions small and intention-revealing.
- Use descriptive variable names based on the DepEd domain.
- Wrap multi-record HR actions in database transactions.
- Keep personnel history append-friendly and auditable.

## Laravel Best Practices

- Prefer Eloquent relationships and scopes over repeated query fragments.
- Avoid hidden N+1 queries.
- Use route model binding where appropriate.
- Use resources or explicit arrays for API responses.
- Do not place database queries in views or React components.
- Do not trust client-side permission checks.
- Do not store sensitive personal data in logs.
- Do not modify authentication flow unless explicitly requested.

## React and Inertia Rules

- Use TypeScript.
- Keep page props explicit and typed.
- Use Inertia forms for server-backed forms.
- Use Wayfinder route helpers when connecting frontend code to Laravel routes.
- Keep components focused and reusable only when reuse is real.
- Avoid duplicating backend business rules in the browser.
- Use accessible controls and clear government HR labels.

## Quality Tools

- PHP formatting: Laravel Pint.
- Static analysis: Larastan/PHPStan.
- Tests: Pest 4.
- Frontend linting: ESLint.
- Frontend formatting: Prettier.
- Frontend type checking: TypeScript.
- Frontend build: Vite.
