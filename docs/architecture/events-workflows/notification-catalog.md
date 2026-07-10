# Notification Catalog

## Purpose

Catalog core notification types, recipients, channels, sensitivity, reminder behavior, and escalation behavior.

| Notification name | Triggering event | Recipient | Channel | Template purpose | Sensitivity | Required action | Reminder schedule | Escalation behavior |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Vacancy published | VacancyPublished | Applicants, HR, school/IU users as configured | In-app, email, portal future | Announce open vacancy. | Medium | View vacancy/apply. | Before closing. | HR if no publication visibility. |
| Application received | ApplicationSubmitted | Applicant, HR intake | In-app, email | Confirm receipt. | Medium | Applicant waits; HR reviews. | None. | HR aging queue. |
| Missing document notice | DocumentaryScreeningCompleted | Applicant/employee-applicant | In-app, email | List deficiency references. | High | Upload/submit documents. | Before deadline. | HR if unresolved. |
| Application screening result | DocumentaryScreeningCompleted | Applicant | In-app, email | Provide screening status. | High | View result. | None. | None unless appeal/correction allowed. |
| Evaluation assignment | WorkflowStepAssigned | Evaluator | In-app, email | Tell evaluator to evaluate. | High | Complete evaluation. | Before due date. | HRMPSB secretariat/HR. |
| Interview schedule | WorkflowStepAssigned | Applicant, interviewer | In-app, email, SMS minimal | Communicate schedule. | Medium | Attend/confirm. | 1 day before. | HR if unconfirmed. |
| HRMPSB meeting notice | WorkflowStepAssigned | HRMPSB members | In-app, email | Meeting notice and packet link. | Restricted | Review packet/attend. | Before meeting. | Chair/secretariat. |
| Deliberation completed | HRMPSBDeliberationCompleted | HR secretariat, appointing authority | In-app, email | Signal recommendation ready. | Restricted | Prepare recommendation/decision. | None. | HR if not acted on. |
| Appointment recommendation result | AppointmentRecommended | Candidate/applicant, HR as policy permits | In-app, email | Communicate status. | High | Proceed or wait. | None. | HR aging queue. |
| Appointment ready for acceptance | AppointmentIssued | Appointee | In-app, email, SMS minimal | Appointment action notice. | High | Accept/acknowledge where applicable. | Before effectivity. | HR. |
| CSC action recorded | CSCActionRecorded | HR, appointee where appropriate | In-app, email | CSC status update. | Restricted | Resolve returned action if needed. | Based on due date. | HR leadership if overdue. |
| Career progression status | CareerAssessmentFinalized | Employee, HR | In-app, email | Status of pathway. | High | Review/comply. | Configured. | Career owner. |
| Reclassification status | ReclassificationApproved | Employee, HR, plantilla manager | In-app, email | Action result. | High | Downstream updates. | None. | HR if updates pending. |
| Competency assessment due | ReminderScheduled | Employee, assessor | In-app, email | Assessment reminder. | High | Complete assessment. | Configured. | Supervisor/HR. |
| IDP approval required | IndividualDevelopmentPlanApproved or WorkflowStepAssigned | Supervisor/HR | In-app, email | Approve IDP. | High | Approve/return. | Before due date. | Office head/HR. |
| Performance rating due | ReminderScheduled | Employee, supervisor | In-app, email | Rating cycle reminder. | Restricted | Submit/validate. | Configured. | Office head/HR. |
| Leave approval required | LeaveApplicationSubmitted | Supervisor/approver | In-app, email | Approve leave. | High | Approve/return/reject. | Before leave date. | Acting/delegated authority. |
| Leave decision | LeaveApplicationApproved | Employee | In-app, email | Inform decision. | High | View result. | None. | None. |
| Attendance correction required | AttendanceAdjustmentSubmitted | Approver/employee | In-app, email | Correction action needed. | High | Review/submit evidence. | Before cutoff. | Payroll/HR if pending. |
| Document verification required | EmployeeDocumentUploaded | Records officer | In-app, email | Verify document. | Restricted | Verify/reject. | Configured. | Records supervisor. |
| Document expiry warning | ReminderScheduled | Employee, HR | In-app, email | Expiring document. | High | Update document. | Configured. | HR if unresolved. |
| Compliance evidence due | ReminderScheduled | Process owner | In-app, email | Submit evidence. | High | Attach/submit evidence. | Before due date. | PRIME-HRM focal. |
| Access review due | ReminderScheduled | System admin, auditor | In-app, email | Review access. | Restricted | Complete review. | Configured. | Security/admin lead. |
| Security-sensitive access detected | RestrictedRecordAccessed | Auditor/security role | In-app, email minimal | Alert access event. | Restricted | Review access. | None. | Security lead. |

## Rule

Notification delivery failure must not reverse or block the underlying approved business action.
