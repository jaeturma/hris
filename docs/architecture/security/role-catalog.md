# Role Catalog

Role names are human-readable. Future Spatie role seeds should use these names unless an approved decision record changes them.

## System Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Super Administrator | Break-glass technical role for full platform administration. | System | System-wide | All system administration, emergency access | Should not perform normal HR workflow approvals | high |
| System Administrator | Maintains system settings and operational configuration. | System | System-wide configuration; limited HR data | Manage users, settings, references | Cannot approve HR decisions unless separately assigned | high |
| Security Administrator | Manages roles, permissions, and access reviews. | System | System-wide security data | Manage roles, permissions, access reviews, audit visibility | Cannot evaluate applicants or approve personnel actions | high |
| Read-only Auditor | Reviews records, audit logs, and compliance evidence. | System / oversight | Assigned audit scope | View audit logs, compliance reports, access logs | Cannot create, update, approve, or delete HR records | high |

## Regional Office Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Regional Director | Regional approving authority and oversight user. | Region | Regional and subordinate offices | Approve workflows, view management dashboards, view compliance reports | Cannot alter evaluation data directly | high |
| Assistant Regional Director | Delegated regional oversight and approvals. | Region | Regional and subordinate offices | Review/approve assigned workflows, reports | Cannot manage security unless separately assigned | high |
| Regional HR Chief | Leads regional HR operations. | Region | Regional and subordinate HR records | Manage HR workflows, review reports, manage HR staff work | Cannot alter audit logs or bypass approvals | high |
| Regional HR Officer | Performs regional HR processing. | Region | Regional assigned workflows | Manage vacancies, employees, plantilla, recruitment, personnel actions | Cannot approve own processed transaction | high |
| Regional Records Officer | Manages regional records and 201 file controls. | Region | Regional records scope | Verify documents, manage records, view document access logs | Cannot evaluate rankings unless separately assigned | high |
| Regional Planning Officer | Supports plantilla, staffing, and analytics. | Region | Regional planning data | View plantilla, reports, dashboards, competency analytics | Cannot view restricted documents by default | medium |
| Regional HRMPSB Chair | Chairs regional HRMPSB cycles. | Region | Assigned HRMPSB cycles | Review evaluations, manage HRMPSB recommendation workflow | Cannot manage system roles or alter criteria after cycle lock | high |
| Regional HRMPSB Member | Participates in regional HRMPSB cycles. | Region | Assigned cycles/applications | Evaluate applications, view assigned documents, submit assessment | Cannot see unrelated applications | high |
| Regional Evaluator | Evaluates assigned applications or competencies. | Region | Assigned applications/assessments | Evaluate applications, interviews, competency assessments | Cannot approve appointment or rankings alone | high |

## Division Office Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Schools Division Superintendent | Division approving authority and oversight user. | Division | Division and subordinate schools/IUs | Approve workflows, view dashboards, view compliance reports | Cannot directly edit evaluation scores | high |
| Assistant Schools Division Superintendent | Delegated division oversight and approvals. | Division | Division and subordinate schools/IUs | Review/approve assigned workflows, reports | Cannot manage security unless separately assigned | high |
| Division HR Chief | Leads division HR operations. | Division | Division HR records | Manage HR workflows, reports, personnel actions | Cannot approve own processed transaction | high |
| Division HR Officer | Performs division HR processing. | Division | Division assigned workflows | Manage vacancies, applications, employees, appointments, personnel actions | Cannot override policy criteria | high |
| Division Records Officer | Manages division records and 201 file controls. | Division | Division records scope | Verify documents, manage records, access logs | Cannot evaluate rankings unless separately assigned | high |
| Division Planning Officer | Supports staffing, plantilla, and analytics. | Division | Division planning data | View plantilla, reports, dashboards | Cannot view restricted documents by default | medium |
| Division HRMPSB Chair | Chairs division HRMPSB cycles. | Division | Assigned HRMPSB cycles | Manage HRMPSB review, recommendations | Cannot approve final appointment unless separately authorized | high |
| Division HRMPSB Member | Participates in division HRMPSB cycles. | Division | Assigned cycles/applications | Evaluate applications, review cycle materials | Cannot see unrelated cycles | high |
| Division Evaluator | Evaluates assigned applications or competencies. | Division | Assigned applications/assessments | Submit evaluations and interview results | Cannot generate final ranking alone | high |

## District / School / Implementing Unit Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Public Schools District Supervisor | District oversight user. | District | Assigned district schools | View district reports, review assigned workflows | Cannot manage division-wide records | medium |
| School Head | School-level approving/recommending authority. | School | Assigned school | Review employees, approve school-level workflows, view reports | Cannot access unrelated school records | high |
| Assistant School Head | Delegated school workflow reviewer. | School | Assigned school | Review assigned workflows, reports | Cannot approve final actions unless delegated | medium |
| School HR Focal Person | School HR processor. | School | Assigned school | Prepare personnel records, documents, leave, reports | Cannot approve own prepared records | high |
| School Records Focal Person | School records support. | School | Assigned school documents | Upload/verify permitted documents, records support | Cannot view restricted documents without permission | high |
| Implementing Unit HR Officer | IU HR processor. | Implementing Unit | Assigned IU | Manage IU HR workflows, documents, leave, reports | Cannot access non-IU records | high |
| Implementing Unit Finance Officer | IU payroll preparation support. | Implementing Unit | Assigned IU payroll prep | View attendance/payroll preparation, export payroll data when authorized | Cannot view restricted HRMPSB records | high |

## Employee / Applicant Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Employee | Authenticated employee self-service user. | Own station | Own records | View own profile, selected documents, leave, IDP, applications | Cannot view other employees | medium |
| Applicant | Authenticated applicant self-service user. | Applicant portal | Own applicant records | Manage own profile, submit applications, upload documents | Cannot view evaluations or rankings unless officially released | medium |
| External Applicant | Applicant without employee linkage. | Applicant portal | Own applicant records | Submit application and documents | Cannot access employee modules | medium |
| Internal Applicant | Employee applying to vacancy/promotion. | Own + application scope | Own employee/application records | Submit internal application, view own status | Cannot view unrelated applicants | high |

## Workflow Roles

| Role | Description | Typical office level | Allowed data scope | Major permissions | Restricted actions | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- |
| Document Verifier | Verifies applicant or employee documents. | Any assigned office | Assigned documents | Verify/reject documents, view document metadata | Cannot approve appointment alone | high |
| Eligibility Screener | Screens applications against QS/checklists. | Any assigned office | Assigned applications | Screen applications, record QS result | Cannot change criteria after lock | high |
| Interview Panel Member | Records interview results. | Cycle-specific | Assigned interviews | Manage assigned interview results | Cannot view unrelated cycle records | high |
| Assessment Panel Member | Scores or assesses assigned criteria. | Cycle-specific | Assigned assessments | Evaluate assigned criteria | Cannot approve final ranking alone | high |
| Approving Officer | Acts on assigned approval step. | Any level | Assigned workflow scope | Approve/reject/return workflows | Cannot approve outside delegation | high |
| Releasing Officer | Releases approved documents or outputs. | Any assigned office | Approved/releasable records | Release appointment documents, reports, outputs | Cannot alter approved basis | high |
