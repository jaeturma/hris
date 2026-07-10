# Navigation Structure

Navigation must be role-aware, permission-aware, and office-scope-aware. Hide unavailable groups in the UI, but enforce all access server-side with Policies.

| Group | Purpose | Target users | Submenus | Required permissions | Priority phase |
| --- | --- | --- | --- | --- | --- |
| Dashboard | Role-based operational landing page. | All users | My Tasks, Metrics, Alerts | Dashboard/report permissions by role | Phase 1 |
| Organization | Manage DepEd hierarchy and stations. | Admin, HR, Planning | Regions, Divisions, Districts, Schools, Implementing Units, Offices, Stations | `regions.manage`, `divisions.manage`, `schools.manage`, `stations.manage` | Phase 1 |
| Employees | Manage employee records and assignments. | HR, Records, Supervisors | Employee Directory, Assignments, Movements, Service Records | `employees.view`, `employees.create`, `employees.update`, `service-records.manage` | Phase 3 |
| Plantilla & Positions | Manage positions and item data. | HR, Planning | Position Titles, Plantilla Items, Salary Grades, Vacant Items | `plantilla.view`, `plantilla.manage`, `position-titles.manage` | Phase 2 |
| Recruitment & Selection | Manage vacancy to appointment pipeline. | HR, HRMPSB, Evaluators | Vacancies, Publications, Applicants, Applications, Screening, CAR/RQA Outputs | `vacancies.manage`, `applications.receive`, `applications.screen` | Phase 4 |
| HRMPSB | Board review and evaluation workspace. | HRMPSB Chair, Members, Evaluators | Assigned Cycles, Evaluations, Interviews, Rankings, Recommendations | `applications.evaluate`, `rankings.manage` | Phase 4 |
| Promotion & Reclassification | Manage career progression and reclassification. | HR, HRMPSB, Approvers | Promotion Cycles, Applications, Reclassification Requests, Readiness | `promotion-cycles.manage`, `reclassification-requests.manage` | Phase 7 |
| Competency-Based HRM | Manage competency framework and assessments. | HR, Competency Admin, Supervisors | Models, Dictionary, Position Profiles, Assessments, Gap Analysis, IDPs | `competency-models.manage`, `competency-assessments.conduct` | Phase 2/5 |
| Performance | Track performance ratings and linkages. | HR, Supervisors, Employees | Rating Periods, Employee Ratings, Performance Linkage | Future performance permissions | Phase 5 |
| Learning & Development | Manage IDPs and interventions. | HR L&D, Supervisors, Employees | IDPs, Interventions, Completion Tracking | `individual-development-plans.manage` | Phase 6 |
| Personnel Records / 201 Files | Manage employee documents and retention. | Records, HR, Auditors | Document Types, Employee Documents, Verification, Access Logs | `employee-documents.view`, `employee-documents.verify` | Phase 3 |
| Leave | Manage leave workflows and ledgers. | Employees, HR, Approvers | Leave Applications, Credits, Ledger | `leave-applications.approve`, `leave-credits.manage` | Phase 9 |
| Attendance | Manage logs, adjustments, and DTR. | Timekeepers, HR, Approvers | Logs, Adjustments, DTR Records | `attendance-logs.manage`, `dtr-records.generate` | Phase 9 |
| Payroll Preparation | Prepare payroll-related records and exports. | Finance, HR, IU Finance | Payroll Periods, Preparation Records, Exports | `payroll-preparation-records.prepare`, `payroll-data.export` | Phase 9 |
| Reports & Analytics | Operational, compliance, PRIME-HRM, and audit reports. | Management, HR, Auditors | Operational Reports, Dashboards, Compliance, PRIME-HRM, Exports | `operational-reports.view`, `reports.export` | Phase 10 |
| System Administration | Configure users, roles, references, and settings. | System/Security Admins | Users, Roles, Permissions, Settings, Reference Data | `users.manage`, `roles.manage`, `permissions.manage` | Phase 1 |
| Audit Trail | Review activity, document, and access logs. | Auditors, Security Admins | Activity Log, Access Logs, Approval History | `audit-logs.view`, `audit-reports.view` | Phase 1 |

## Navigation Rules

- Badge groups with task counts only when counts are scoped and authorized.
- Do not show HRMPSB cycles to unassigned members.
- Do not show restricted document links without explicit permission.
- Employee and applicant navigation should be simpler than HR/admin navigation.
