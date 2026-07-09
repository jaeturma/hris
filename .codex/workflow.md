# Codex Development Workflow

Use this workflow for future development in `D:\lara\www\hris`.

## Before Coding

1. Read `AGENTS.md` and the relevant `.codex/*.md` files.
2. Inspect existing Laravel, React, Inertia, and database patterns.
3. Identify whether the task touches DepEd policy, personal data, authorization, audit trail, or government records.
4. Confirm the affected office scope: Region, Division, District, School, or Implementing Unit.
5. Define permissions and audit events before writing feature code.

## During Coding

- Keep implementation narrow.
- Do not change auth flow unless explicitly requested.
- Do not install packages unless explicitly approved.
- Use Laravel conventions and existing project patterns.
- Use Spatie Permission for authorization.
- Use Spatie Activitylog for audit trails.
- Use MySQL-friendly migrations and queries.
- Use Inertia React with typed props and Wayfinder route helpers.

## Before Finishing

Run the most relevant checks:

- PHP formatting: `composer lint`
- Static analysis: `composer types:check`
- Tests: `php artisan test --compact`
- Frontend lint: `npm run lint:check`
- Frontend format check: `npm run format:check`
- Frontend types: `npm run types:check`
- Frontend build: `npm run build`

For small documentation-only changes, no application test run is required unless requested.

## Delivery Notes

Final responses should include files changed, behavior or documentation added, checks run or not run, assumptions, and recommended next step.

## Local Environment

- Project path: `D:\lara\www\hris`
- Local URL: `https://hris.app`
- Environment: Laragon on Windows
- Frontend build: Vite
