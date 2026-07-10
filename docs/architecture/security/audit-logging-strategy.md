# Audit Logging Strategy

Use Spatie Laravel Activitylog for user-facing audit events and add specialized access logs where needed for sensitive view/export events.

## Audit Principles

- Log important actions, not every low-value page view.
- Include actor, subject, event, office scope, timestamp, workflow state, and safe changed fields.
- Avoid logging full personal data, document contents, or sensitive remarks.
- Keep audit logs readable only by authorized auditors/security users.
- Preserve audit history for official HR actions.

## Actions Requiring Audit Logging

| Area | Example events |
| --- | --- |
| Security | user created, role assigned, permission changed, account disabled |
| Organization | region/division/school/station changed |
| Employee | employee created, sensitive info updated, assignment changed, movement created |
| Plantilla | item marked vacant, item assigned, salary grade changed |
| Recruitment | vacancy published, application screened, document verified, evaluation changed |
| HRMPSB | assessment submitted, ranking generated, recommendation created |
| Appointment | appointment recommended, approved, returned, released |
| Promotion/Reclassification | application evaluated, request approved/rejected, evidence changed |
| Competency | dictionary changed, profile approved, assessment submitted, IDP approved |
| Documents | restricted document viewed/downloaded, document verified/replaced |
| Leave/Attendance/Payroll | leave approved, attendance adjusted, DTR generated, payroll exported |
| Reports | compliance report exported, audit report viewed, PRIME-HRM report exported |

## Event Naming

Use predictable event names:

- `created`
- `updated`
- `submitted`
- `verified`
- `approved`
- `rejected`
- `returned`
- `cancelled`
- `released`
- `exported`
- `viewed-restricted`

## Access Logs vs Activity Logs

Use activity logs for state-changing actions. Use dedicated access logs for sensitive view/download/export events that may become high-volume or require retention rules.
