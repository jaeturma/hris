# Enterprise Domain Model

This folder defines the enterprise business domains and bounded contexts for HRIS for DepEd. It is documentation only and must not be treated as generated application structure.

## Purpose

The domain model prevents future modules from becoming scattered across generic Laravel folders. Domains identify who owns business rules, write operations, policy interpretation, audit history, and reports.

## Domain Rules

- A domain owns its core business rules and write operations.
- Other domains may read through defined interfaces, reports, events, or application actions but must not directly modify another domain's records.
- Policy-driven rules must be resolved through the Policy and Configuration Domain.
- Reports may read across domains but must not own operational source records.
- Integration adapters translate external data into application commands or events; they must not contain core HR logic.
- Competency management is a core domain, not a future add-on.
- Recruitment, appointment, and career progression are separate domains.
- Uploaded documents are evidence records, not substitutes for structured HR data.

## Domains

| Domain | File |
| --- | --- |
| Core Platform | `core-platform-domain.md` |
| Organization | `organization-domain.md` |
| Workforce | `workforce-domain.md` |
| Plantilla and Position | `plantilla-position-domain.md` |
| Recruitment and Selection | `recruitment-selection-domain.md` |
| Appointment and Personnel Action | `appointment-personnel-action-domain.md` |
| Career Progression | `career-progression-domain.md` |
| Competency | `competency-domain.md` |
| Performance | `performance-domain.md` |
| Learning and Development | `learning-development-domain.md` |
| Personnel Records | `personnel-records-domain.md` |
| Leave | `leave-domain.md` |
| Attendance | `attendance-domain.md` |
| Payroll Preparation | `payroll-preparation-domain.md` |
| Rewards and Recognition | `rewards-recognition-domain.md` |
| Employee Relations | `employee-relations-domain.md` |
| Governance and Compliance | `governance-compliance-domain.md` |
| Reporting and Analytics | `reporting-analytics-domain.md` |
| Integration | `integration-domain.md` |
| Policy and Configuration | `policy-configuration-domain.md` |

## Architecture Decisions

1. Project remains named HRIS for DepEd.
2. DepEd-specific policy takes priority for DepEd workflows.
3. CSC frameworks provide government-wide alignment.
4. Policy rules are versioned and configurable.
5. Domains own business rules and write operations.
6. Reports may read across domains but do not own source records.
7. Competency management is a core domain.
8. Recruitment, appointment, and career progression remain separate domains.
9. Uploaded documents and structured records remain distinct.
10. Multi-office data scope is foundational.
11. AI features remain advisory and require human validation.
12. Sensitive employee-relations records require restricted architecture.

## Implementation Note

Do not create Laravel domain folders, React feature folders, migrations, models, policies, or events from this document until an implementation phase explicitly authorizes code.
