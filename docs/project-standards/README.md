# Project Standards

These standards govern future development of the DepEd HRIS in `D:\lara\www\hris`.

The project is a Laravel 13 + React + Inertia + MySQL system for Philippine government HR operations serving Regional Offices, Schools Division Offices, Implementing Units, and Large Schools. Standards must support Civil Service Commission compliance, Data Privacy Act obligations, auditability, personnel records, recruitment, hiring, promotion, plantilla management, employee records, and HRMPSB processes.

No HRIS module, migration, route, controller, or UI page should be created until the relevant standard here has been considered.

## Standards Index

- `naming-conventions.md`: names for backend, frontend, database, roles, permissions, and seeders.
- `folder-structure.md`: recommended enterprise folder structure for Laravel and React.
- `coding-standards.md`: coding rules and Laravel best practices.
- `database-standards.md`: schema rules for large-scale government HR data.
- `ui-design-system.md`: accessible, restrained, government-ready UI specification.
- `permission-strategy.md`: RBAC, policies, gates, and approval workflow philosophy.
- `architecture-principles.md`: architectural decision rules for future modules.
- `api-guidelines.md`: future API rules even though the first UI uses Inertia.
- `testing-standards.md`: Pest testing expectations and coverage targets.
- `git-workflow.md`: branches, commits, pull requests, releases, and reviews.

## Global Engineering Rules

- Follow Laravel conventions first.
- Preserve official HR history instead of silently overwriting records.
- Enforce authorization on the server.
- Protect sensitive personal and employment data.
- Log significant record changes with Spatie Laravel Activitylog.
- Use Spatie Laravel Permission for roles and permissions.
- Use Pest 4, Laravel Pint, Larastan/PHPStan, ESLint, Prettier, TypeScript, and Vite checks as appropriate.
- Do not quote full legal or policy text in code or docs; document engineering implications and verify exact rules from official sources when required.
