# Architecture Rules

This project is a DepEd HRIS built with Laravel 13, React, Inertia, MySQL, Vite, Spatie Laravel Permission, and Spatie Laravel Activitylog. Design it as a long-lived government records system.

## Architectural Principles

- Keep Laravel as the system of record and Inertia React as the user interface layer.
- Use MySQL for relational HR records; avoid storing authoritative personnel state only in JSON blobs.
- Preserve history for personnel actions. Appointments, promotions, transfers, reclassifications, separations, leave activity, and service records must be append-friendly and auditable.
- Keep modules bounded by HR business capability, not by screen names.
- Prefer Laravel Form Requests, policies or permission checks, service/action classes, Eloquent relationships, events, and jobs where they match existing project patterns.
- Do not bypass Inertia with ad hoc API patterns unless a future requirement explicitly needs an API boundary.

## Government Office Model

Architecture must support Region offices, Schools Division Offices, Districts, Schools, Implementing Units, and Large Schools. Do not assume all users belong to a single school or division. Design office scoping deliberately so regional users can oversee divisions, division users can manage schools, and school or implementing-unit users can operate within assigned limits.

## Module Boundaries

Future modules should be planned around organizational structure, employee profiles and 201 files, plantilla and position management, recruitment, HRMPSB workflows, appointments, promotions, reclassification, transfers, separations, service records, leave management, performance ratings, reports, administration, roles, permissions, and audit logs.

Before creating a module, document purpose, users, policy area, data ownership, office scope, state transitions, permissions, audit events, reports, retention needs, Pest tests, and static analysis checks.

## Inertia Boundaries

- Controllers prepare page props and delegate complex work to services, queries, or actions.
- React pages should receive explicit, minimal props rather than hidden global state.
- Use Wayfinder-generated route helpers where frontend code calls Laravel routes.
- Avoid hardcoded URLs except for external references and the configured local URL `https://hris.app`.

## Background Work

Use jobs for slow or retryable work such as bulk imports, report generation, exports, notifications, and record synchronization. Jobs that touch personnel records must be idempotent, auditable, and permission-safe at dispatch time.

## Reporting

Reports must be reproducible. Store enough filters, timestamps, office scope, and user context to explain how a report was produced. Exports containing personal information must be permission-gated and activity-logged.
