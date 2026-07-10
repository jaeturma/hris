# Dashboard Strategy

Dashboards must be role-based, office-scoped, and action-oriented. They should help users process work, not decorate the app.

## Dashboard Types

| Dashboard | Primary users | Widgets | Notes |
| --- | --- | --- | --- |
| Super Admin Dashboard | Super Administrator | System health, user counts, role changes, audit alerts | No HR decision shortcuts by default |
| Regional HR Dashboard | Regional HR Chief/Officer | Regional vacancies, appointment pipeline, division summaries, PRIME-HRM readiness, competency gaps | Aggregate division data with drilldown |
| Division HR Dashboard | Division HR Chief/Officer | Vacancies, applications, HRMPSB cycles, appointments, school staffing, document tasks | Daily operations focus |
| School / IU HR Dashboard | School HR Focal, IU HR Officer | Staff list, pending documents, leave tasks, attendance issues, personnel movement status | Local scope only |
| HRMPSB Dashboard | HRMPSB Chair/Member, Evaluator | Assigned cycles, applications to review, interview schedule, missing evaluations, ranking status | Cycle-limited access |
| Employee Dashboard | Employee | Own profile status, leave balance, applications, IDP, documents needing update | Own-record only |
| Applicant Dashboard | Applicant, External Applicant, Internal Applicant | Application status, missing documents, interview notices, submitted documents | Own application only |
| Auditor Dashboard | Read-only Auditor | Audit queues, sensitive access logs, report exports, compliance views | Read-only and scoped |

## Widget Standards

- Use compact cards for counts and alerts.
- Use tables or task lists for actionable work.
- Include filters for office scope and period where authorized.
- Show last updated timestamp for operational metrics.
- Avoid charts unless they clarify trends or compliance status.

## Common Widgets

- Pending approvals.
- Missing document verification.
- Open vacancies.
- Applications for screening.
- HRMPSB evaluation backlog.
- Appointment tracking status.
- Service record update tasks.
- Competency gap summary.
- Leave pending approval.
- Attendance correction pending approval.
- Audit alerts.

## Dashboard Risks

- Do not aggregate data that exposes sensitive records to unauthorized users.
- Do not show evaluator scores or HRMPSB details outside assigned cycles.
- Do not allow dashboard quick actions to bypass workflow validation.
