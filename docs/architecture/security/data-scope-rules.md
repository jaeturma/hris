# Data Scope Rules

Permissions answer what an actor may do. Data scope answers which records the actor may act on.

## Scope Types

| Scope | Description | Example |
| --- | --- | --- |
| System-wide access | Access across all offices and records, reserved for carefully controlled system/security/audit functions. | Super Administrator, Read-only Auditor with approved scope |
| Regional access | Access to a Region and subordinate divisions, districts, schools, and IUs. | Regional HR Chief |
| Division access | Access to a Division and subordinate districts, schools, and IUs. | Division HR Officer |
| District access | Access to assigned district and schools for oversight/reporting. | Public Schools District Supervisor |
| School / Implementing Unit access | Access only to assigned school or IU records. | School HR Focal Person |
| Own-record access | Access only to the authenticated employee's own records. | Employee |
| Applicant self-service access | Access only to the applicant's profile, applications, and submitted documents. | External Applicant |
| HRMPSB limited-cycle access | Access only to assigned recruitment/promotion cycle records. | HRMPSB Member |
| Evaluator limited-assignment access | Access only to assigned applications, interviews, or competency assessments. | Evaluator |

## Rules

- Scope must be enforced in Laravel Policies or query scopes, not only in UI filters.
- Role assignment should include office context where needed.
- HRMPSB and evaluator assignments must expire or close with the cycle.
- Applicant and employee self-service must never infer access from predictable IDs.
- Reports must apply the same office scope and document sensitivity rules as pages.
- Exports must include scope metadata and be audit-logged.

## Policy Requirements

Future Policies should check:

- Permission name.
- Office scope.
- Workflow assignment.
- Record sensitivity.
- Workflow state.
- Self-service ownership.
- Whether the user is the actor who created/prepared the record.

## Scope Risk Notes

- Regional access must not become implicit system-wide access.
- Division users must not see other divisions through search, exports, dashboards, or autocomplete.
- School/IU users must not see division-wide applicant or employee data unless explicitly assigned.
- HRMPSB members must not retain access after a cycle closes unless policy allows archival access.
