# Permission Matrix

## Naming Conventions

- Spatie guard: `web`.
- Role names: Title Case human-readable names, for example `Division HR Officer`.
- Permission names: plural resource plus action, using kebab-case resources and dot actions, for example `employees.view-sensitive`, `appointments.approve`.
- Avoid vague permissions such as `manage all`, `admin`, or `process`.

## Permission Groups

### A. System Administration

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage users | `users.manage` | Super Administrator, System Administrator | yes |
| manage roles | `roles.manage` | Super Administrator, Security Administrator | yes |
| manage permissions | `permissions.manage` | Super Administrator, Security Administrator | yes |
| manage system settings | `system-settings.manage` | Super Administrator, System Administrator | yes |
| view audit logs | `audit-logs.view` | Super Administrator, Security Administrator, Read-only Auditor | yes |

### B. Organization Management

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage regions | `regions.manage` | Super Administrator, System Administrator | yes |
| manage divisions | `divisions.manage` | Regional HR Chief, System Administrator | yes |
| manage districts | `districts.manage` | Division HR Chief, Division Planning Officer | yes |
| manage schools | `schools.manage` | Division HR Chief, Division Planning Officer | yes |
| manage offices | `offices.manage` | Regional/Division HR Chief | yes |
| manage office units | `office-units.manage` | Regional/Division HR Chief | yes |
| manage stations | `stations.manage` | Regional/Division HR Officer | yes |

### C. Employee Management

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| view employees | `employees.view` | HR roles, supervisors, auditors | conditional |
| create employees | `employees.create` | Regional/Division HR Officer | yes |
| update employees | `employees.update` | HR Officer, Records Officer | yes |
| archive employees | `employees.archive` | HR Chief, System Administrator | yes |
| view sensitive employee information | `employees.view-sensitive` | HR Chief, Records Officer, Auditor | yes |
| manage employee assignments | `employee-assignments.manage` | HR Officer | yes |
| manage employee movements | `employee-movements.manage` | HR Officer | yes |
| manage service records | `service-records.manage` | Records Officer | yes |

### D. Plantilla and Position

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| view plantilla | `plantilla.view` | HR, Planning, Management | no |
| manage plantilla | `plantilla.manage` | HR Chief, Planning Officer | yes |
| manage position titles | `position-titles.manage` | HR Chief, System Administrator | yes |
| manage salary grades | `salary-grades.manage` | System Administrator, HR Chief | yes |
| manage item numbers | `item-numbers.manage` | HR/Planning Officer | yes |
| mark item as vacant | `plantilla-items.mark-vacant` | HR Officer | yes |
| assign item to employee | `plantilla-items.assign` | HR Officer | yes |

### E. Recruitment, Selection, and Appointment

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage vacancies | `vacancies.manage` | HR Officer | yes |
| publish vacancies | `vacancies.publish` | HR Chief, Approving Officer | yes |
| receive applications | `applications.receive` | HR Officer | yes |
| screen applications | `applications.screen` | Eligibility Screener | yes |
| evaluate applications | `applications.evaluate` | Evaluator, HRMPSB Member | yes |
| manage interviews | `interviews.manage` | Interview Panel Member | yes |
| manage rankings | `rankings.manage` | HRMPSB Chair, HR Officer | yes |
| generate comparative assessment result | `comparative-assessment-results.generate` | HR Officer, HRMPSB Chair | yes |
| recommend appointment | `appointment-recommendations.create` | HRMPSB Chair, HR Chief | yes |
| approve appointment | `appointments.approve` | Approving Officer, RD, SDS | yes |
| release appointment documents | `appointment-documents.release` | Releasing Officer, Records Officer | yes |

### F. Promotion and Reclassification

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage promotion cycle | `promotion-cycles.manage` | HR Chief, HR Officer | yes |
| receive promotion applications | `promotion-applications.receive` | HR Officer | yes |
| evaluate promotion applications | `promotion-applications.evaluate` | Evaluator, HRMPSB Member | yes |
| manage reclassification requests | `reclassification-requests.manage` | HR Officer | yes |
| approve reclassification | `reclassification-requests.approve` | Approving Officer, RD/SDS | yes |
| generate promotion reports | `promotion-reports.generate` | HR Officer, HR Chief | yes |

### G. Competency-Based HRM

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage competency models | `competency-models.manage` | HR Chief, Competency Administrator | yes |
| manage competency dictionary | `competency-dictionary.manage` | Competency Administrator | yes |
| manage position competency profiles | `position-competency-profiles.manage` | HR Planning, HR Chief | yes |
| conduct competency assessments | `competency-assessments.conduct` | Evaluator, Supervisor | yes |
| view competency gap analysis | `competency-gap-analyses.view` | HR, Supervisor, Employee own view | yes |
| manage individual development plans | `individual-development-plans.manage` | HR, Supervisor | yes |
| view succession readiness | `succession-readiness.view` | HR Chief, Management, Auditor | yes |

### H. Personnel Records / 201 Files

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| upload employee documents | `employee-documents.upload` | Records Officer, HR Focal | yes |
| verify employee documents | `employee-documents.verify` | Document Verifier, Records Officer | yes |
| view employee documents | `employee-documents.view` | HR, Records, Employee own view | yes |
| view restricted documents | `employee-documents.view-restricted` | Records Officer, Auditor, HR Chief | yes |
| manage document types | `document-types.manage` | Records Officer, System Administrator | yes |
| manage retention rules | `records-retention-rules.manage` | Records Officer, System Administrator | yes |
| view document access logs | `document-access-logs.view` | Records Officer, Auditor, Security Administrator | yes |

### I. Leave, Attendance, Payroll

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| manage leave types | `leave-types.manage` | HR Leave Administrator | yes |
| manage leave credits | `leave-credits.manage` | HR Leave Administrator | yes |
| approve leave applications | `leave-applications.approve` | Approving Officer, School Head | yes |
| manage attendance logs | `attendance-logs.manage` | Timekeeper, HR Officer | yes |
| approve attendance adjustments | `attendance-adjustments.approve` | Approving Officer | yes |
| generate DTR | `dtr-records.generate` | Timekeeper, HR Officer | yes |
| prepare payroll records | `payroll-preparation-records.prepare` | Finance Officer, Payroll Staff | yes |
| export payroll data | `payroll-data.export` | Finance Officer | yes |

### J. Reports and Analytics

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| view operational reports | `operational-reports.view` | HR, Management | conditional |
| view management dashboards | `management-dashboards.view` | RD, SDS, HR Chief | conditional |
| view compliance reports | `compliance-reports.view` | HR Chief, Auditor | yes |
| export reports | `reports.export` | Authorized HR/Records/Auditor | yes |
| view PRIME-HRM readiness reports | `prime-hrm-reports.view` | HR Chief, Management, Auditor | yes |
| view audit reports | `audit-reports.view` | Auditor, Security Administrator | yes |

### K. Workflow and Approvals

| Permission | Recommended name | Typical roles | Audit required |
| --- | --- | --- | --- |
| initiate workflow | `workflows.initiate` | HR roles, Employee where applicable | yes |
| review workflow | `workflows.review` | Reviewer, HRMPSB roles | yes |
| approve workflow | `workflows.approve` | Approving Officer | yes |
| reject workflow | `workflows.reject` | Approving Officer | yes |
| return workflow | `workflows.return` | Reviewer, Approving Officer | yes |
| cancel workflow | `workflows.cancel` | Workflow owner, HR Chief | yes |
| view approval history | `approval-history.view` | HR, Approvers, Auditors | yes |
