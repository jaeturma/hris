# Data Architecture and Reference Masterlist

This folder defines the high-level data architecture for the DepEd-first, PRIME-HRM-aligned, competency-based HRIS. It is documentation only. Do not create migrations, models, routes, controllers, seeders, or React pages from this masterlist until the related module is approved and manually verified against current DepEd and CSC guidance.

## Design Rules

- Support Region, Division, District, School, Implementing Unit, and Office / Unit; never assume one office.
- Preserve official HR history and document history.
- Keep applicant, employee, plantilla, competency, recruitment, promotion, records, leave, attendance, payroll, security, and audit data in clear boundaries.
- Treat competency mapping as foundational for recruitment, placement, performance, learning and development, promotion, reclassification, succession readiness, and rewards.
- Use MySQL-friendly relational tables with foreign keys, indexes, and explicit status fields.
- Use Spatie Permission tables for RBAC and Spatie Activitylog for user-facing activity trails.
- Design for future attendance devices, payroll exports, and document storage integration.

## Data Groups

| File | Purpose |
| --- | --- |
| `core-reference-tables.md` | Shared lookup and reference data. |
| `organization-structure.md` | Region, Division, District, School, Implementing Unit, office, unit, and station data. |
| `personnel-master-data.md` | Employee identity, personal, employment, assignment, movement, and service records. |
| `plantilla-position-data.md` | Position titles, plantilla items, salary grades, job families, and appointment references. |
| `competency-data.md` | CBHRMS competency library, mappings, assessments, gaps, and IDPs. |
| `recruitment-selection-data.md` | Vacancy, application, evaluation, HRMPSB, ranking, and appointment data. |
| `promotion-reclassification-data.md` | Promotion, career progression, reclassification, support documents, and approvals. |
| `personnel-records-data.md` | 201 files, documents, verification, access logs, and retention rules. |
| `leave-attendance-payroll-data.md` | Leave, attendance, DTR, payroll preparation, and integration-ready records. |
| `audit-security-data.md` | Users, roles, permissions, activity logs, approvals, and access logs. |
| `seeders-and-reference-data.md` | Seeder strategy and manually verified reference data requirements. |

## Notes Before Migration Creation

- Confirm exact DepEd and CSC policy requirements before adding constraints or seed data.
- Decide whether public-facing references need UUIDs before migration design.
- Create reference and organization tables before workflow tables.
- Define audit event names and document classifications before records modules.
