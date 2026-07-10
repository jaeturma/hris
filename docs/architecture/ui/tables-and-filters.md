# Tables and Filters

Tables are primary work surfaces for HR operations. They must be dense, readable, filterable, permission-aware, and export-safe.

## Table Standards

- Default to paginated tables for large datasets.
- Use sticky headers only when they improve scanning.
- Show status badges with text.
- Include row-level actions in a menu.
- Disable or hide actions the user cannot perform, but enforce permissions server-side.
- Include empty, loading, and error states.

## Search and Filters

Common filters:

- Office scope.
- Status.
- Date range.
- Position title.
- Salary grade.
- Item number.
- School / Implementing Unit.
- Vacancy.
- Workflow step.
- Document verification status.
- HRMPSB cycle.
- Competency category or gap.

## Export Rules

- Export buttons require explicit permission.
- Exports should show selected filters before generation.
- Sensitive exports require confirmation.
- Export activity must be logged.
- Exports should include generation time, requesting user, and office scope.

## Bulk Actions

Use bulk actions carefully. Good candidates:

- Mark notifications read.
- Generate selected reports.
- Assign evaluator to selected applications.

Avoid bulk destructive or final approval actions unless a later policy decision explicitly allows them.

## Table Types

| Table | Required columns |
| --- | --- |
| Employee directory | Name, employee number, station, position, status, actions |
| Plantilla items | Item number, position title, salary grade, station, occupancy status |
| Applications | Applicant, vacancy, status, document completeness, screening result |
| HRMPSB evaluations | Applicant, criteria status, evaluator, interview status, ranking status |
| Documents | Type, owner, status, verification, last updated, access action |
| Audit logs | Event, actor, subject, office scope, timestamp |
