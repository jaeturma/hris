# Codex Workspace Rules for DepEd HRIS

This repository is a Laravel 13 + React + Inertia HRIS for Philippine government use, especially DepEd Regional Offices, Schools Division Offices, Implementing Units, and Large Schools. Codex must treat it as a government-grade HR information system, not a generic private-company HR app.

## Global Rules

- Do not modify Laravel core, vendor code, generated framework internals, or authentication flow unless the user explicitly asks for that work.
- Do not install packages unless the user explicitly approves the package and reason.
- Do not create HRIS modules before the module scope, policy basis, data model, authorization matrix, audit events, and tests are documented.
- Prefer existing Laravel, React, Inertia, Vite, Tailwind, and project conventions over new abstractions.
- Keep changes small, reviewable, and aligned with `D:\lara\www\hris`.
- Use the local development URL `https://hris.app` under Laragon on Windows.
- Run the narrowest relevant verification first, then broader checks when warranted.

## Project Stack

- Backend: Laravel 13, PHP 8.3, MySQL
- Frontend: React 19, Inertia v3, TypeScript, Vite, Tailwind CSS
- Authorization: Spatie Laravel Permission
- Audit trail: Spatie Laravel Activitylog
- Testing: Pest 4
- Static analysis: Larastan / PHPStan
- Formatting: Laravel Pint, Prettier, ESLint
- AI assistant: Codex

## DepEd Domain

All future development must understand these entities and processes:

- Governance structure: Region, Division, District, School, Implementing Unit
- Workforce structure: Employee, Plantilla Item, Position Title, Salary Grade, Item Number
- Personnel actions: Appointment, Promotion, Reclassification, Transfer, Separation
- HR records: Service Record, Leave Management, 201 Files, Performance Rating
- Merit and selection: HRMPSB, Recruitment, Hiring, Placement, Promotion, Qualification Standards
- Controls: Audit Trail, Role-based Access Control, Data Privacy

## Policy Awareness

Use policy-aware guidance without quoting full legal text. Validate detailed rules against current official sources before implementing production logic.

- DepEd hiring, placement, and promotion guidelines
- DepEd Order No. 007, s. 2023
- DepEd Order No. 020, s. 2024
- DepEd Order No. 024, s. 2025
- Civil Service Commission rules
- Data Privacy Act
- Government records management requirements

## Engineering Expectations

- Every sensitive workflow must define who can view, create, update, approve, export, and audit the record.
- Every personnel action must preserve history; do not overwrite government HR records without an audit-safe model.
- Every module must include audit events, validation rules, authorization checks, database constraints, and Pest coverage.
- Avoid hardcoded office assumptions. Model Region, Division, District, School, and Implementing Unit boundaries explicitly.
- Treat 201 files, leave records, ratings, appointments, and item data as sensitive personal and employment information.
- Avoid speculative features. Build only what the user asks for and document assumptions.

## Documentation Map

- `.codex/architecture.md`: system boundaries and module architecture
- `.codex/deped.md`: DepEd domain and policy-aware rules
- `.codex/coding-standards.md`: backend and frontend code conventions
- `.codex/database.md`: MySQL schema and data modeling rules
- `.codex/security.md`: privacy, RBAC, audit, and records controls
- `.codex/testing.md`: Pest, Larastan/PHPStan, Pint, and frontend checks
- `.codex/ui.md`: government-grade Inertia React interface rules
- `.codex/workflow.md`: repeatable Codex development workflow
- `.codex/prompts/`: reusable prompts for future Codex tasks
# Codex Workspace Rules for DepEd HRIS

This repository is a Laravel 13 + React + Inertia HRIS for Philippine government use, especially DepEd Regional Offices, Schools Division Offices, Implementing Units, and Large Schools. Codex must treat it as a government-grade HR information system, not a generic private-company HR app.

## Global Rules

- Do not modify Laravel core, vendor code, generated framework internals, or authentication flow unless the user explicitly asks for that work.
- Do not install packages unless the user explicitly approves the package and reason.
- Do not create HRIS modules before the module scope, policy basis, data model, authorization matrix, audit events, and tests are documented.
- Prefer existing Laravel, React, Inertia, Vite, Tailwind, and project conventions over new abstractions.
- Keep changes small, reviewable, and aligned with `D:\lara\www\hris`.
- Use the local development URL `https://hris.app` under Laragon on Windows.
- Run the narrowest relevant verification first, then broader checks when warranted.

## Project Stack

- Backend: Laravel 13, PHP 8.3, MySQL
- Frontend: React 19, Inertia v3, TypeScript, Vite, Tailwind CSS
- Authorization: Spatie Laravel Permission
- Audit trail: Spatie Laravel Activitylog
- Testing: Pest 4
- Static analysis: Larastan / PHPStan
- Formatting: Laravel Pint, Prettier, ESLint
- AI assistant: Codex

## DepEd Domain

All future development must understand these entities and processes:

- Governance structure: Region, Division, District, School, Implementing Unit
- Workforce structure: Employee, Plantilla Item, Position Title, Salary Grade, Item Number
- Personnel actions: Appointment, Promotion, Reclassification, Transfer, Separation
- HR records: Service Record, Leave Management, 201 Files, Performance Rating
- Merit and selection: HRMPSB, Recruitment, Hiring, Placement, Promotion, Qualification Standards
- Controls: Audit Trail, Role-based Access Control, Data Privacy

## Policy Awareness

Use policy-aware guidance without quoting full legal text. Validate detailed rules against current official sources before implementing production logic.

- DepEd hiring, placement, and promotion guidelines
- DepEd Order No. 007, s. 2023
- DepEd Order No. 020, s. 2024
- DepEd Order No. 024, s. 2025
- Civil Service Commission rules
- Data Privacy Act
- Government records management requirements

## Engineering Expectations

- Every sensitive workflow must define who can view, create, update, approve, export, and audit the record.
- Every personnel action must preserve history; do not overwrite government HR records without an audit-safe model.
- Every module must include audit events, validation rules, authorization checks, database constraints, and Pest coverage.
- Avoid hardcoded office assumptions. Model Region, Division, District, School, and Implementing Unit boundaries explicitly.
- Treat 201 files, leave records, ratings, appointments, and item data as sensitive personal and employment information.
- Avoid speculative features. Build only what the user asks for and document assumptions.

## Documentation Map

- `.codex/architecture.md`: system boundaries and module architecture
- `.codex/deped.md`: DepEd domain and policy-aware rules
- `.codex/coding-standards.md`: backend and frontend code conventions
- `.codex/database.md`: MySQL schema and data modeling rules
- `.codex/security.md`: privacy, RBAC, audit, and records controls
- `.codex/testing.md`: Pest, Larastan/PHPStan, Pint, and frontend checks
- `.codex/ui.md`: government-grade Inertia React interface rules
- `.codex/workflow.md`: repeatable Codex development workflow
- `.codex/prompts/`: reusable prompts for future Codex tasks
