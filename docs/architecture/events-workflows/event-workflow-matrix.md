# Event and Workflow Matrix

## Purpose

Map representative HRIS commands to domain events, workflow transitions, listeners, notifications, queues, audits, owning domains, and policy dependencies.

| Business process | Command | Domain event | Workflow state transition | Listener or consumer | Notification | Queue usage | Audit requirement | Owning domain | Policy dependency |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Vacancy publication | PublishVacancy | VacancyPublished | For Approval -> Open | Notifications, Reporting | Vacancy published | Notify applicants/HR | Publication snapshot | Recruitment | DepEd hiring, MSP |
| Applicant submission | SubmitApplication | ApplicationSubmitted | Draft -> Submitted | HR intake | Application received | Notify HR/applicant | Submission snapshot | Recruitment | Data Privacy, DepEd hiring |
| Document screening | CompleteDocumentaryScreening | DocumentaryScreeningCompleted | Under Review -> For Evaluation/Awaiting Documents | Applicant notification | Missing document/result | Notify applicant | Screening history | Recruitment | DepEd documentary rules |
| QS validation | ValidateQualificationStandards | ApplicantQualified/ApplicantDisqualified | For Evaluation -> For Evaluation/Rejected | HRMPSB packet | Screening result | Optional | QS snapshot | Recruitment | CSC QS, DepEd |
| Evaluation | FinalizeEvaluation | EvaluationFinalized | For Evaluation -> For Deliberation | HRMPSB | Evaluation assignment complete | Optional | Immutable evaluation | Recruitment | Assessment framework |
| Interview | CompleteInterview | InterviewCompleted | For Interview -> For Evaluation | Evaluators | Interview status | Optional | Interview record | Recruitment | DepEd cycle rules |
| HRMPSB deliberation | CompleteDeliberation | HRMPSBDeliberationCompleted | For Deliberation -> For Recommendation | Appointment, Governance | Deliberation completed | Optional | Quorum/recusal history | Recruitment | HRMPSB/MSP |
| Ranking output | GenerateRanking | RankingGenerated | For Recommendation -> Released | Reporting | Ranking ready | Report job optional | Report version | Recruitment | DepEd output rules |
| Appointment recommendation | RecommendAppointment | AppointmentRecommended | For Recommendation -> For Approval | Appointment domain | Recommendation result | Optional | Recommendation history | Recruitment | DepEd/CSC appointment |
| Appointment issuance | IssueAppointment | AppointmentIssued | For Approval -> Released | Workforce, Plantilla, Records | Appointment ready | Side effects queued | Appointment history | Appointment | CSC ORAOHRA |
| CSC submission | SubmitAppointmentToCSC | AppointmentSubmittedToCSC | Submitted -> Under Review | Governance | CSC submitted | Integration future | Submission log | Appointment | CSC ORAOHRA |
| CSC action | RecordCSCAction | CSCActionRecorded | Under Review -> Finalized/Returned | Workforce, Records | CSC action recorded | Notify HR/appointee | CSC action history | Appointment | CSC ORAOHRA |
| Onboarding | CreateEmployeeFromAppointment | EmployeeCreated | Open -> Finalized | Records, Payroll prep | Onboarding tasks | Side effects queued | Employee creation audit | Workforce | DepEd personnel admin |
| Plantilla assignment | EncumberItem | ItemEncumbered | Under Review -> Finalized | Workforce, Reporting | HR notice | Optional | Item history | Plantilla | Plantilla/appointment |
| Personnel movement | RecordPersonnelMovement | PersonnelMovementRecorded | For Approval -> Finalized | Workforce, Attendance, Payroll | Movement status | Side effects queued | Movement history | Appointment | DepEd/CSC action |
| Higher teaching promotion | FinalizeHigherTeachingAssessment | CareerAssessmentFinalized | For Evaluation -> For Approval | HRMPSB/Appointment | Career status | Optional | Assessment snapshot | Career Progression | DepEd higher teaching |
| Expanded career progression | SubmitCareerProgression | CareerProgressionApplicationSubmitted | Draft -> Submitted | HR/evaluator | Career progression status | Notify HR | Submission history | Career Progression | DepEd career progression |
| Reclassification | ApproveReclassification | ReclassificationApproved | For Approval -> Finalized | Plantilla, Appointment, Records | Reclassification status | Side effects queued | Approval/item impact | Career Progression | DepEd/CSC |
| Competency assessment | CompleteCompetencyAssessment | CompetencyAssessmentCompleted | For Evaluation -> Finalized | L&D, Career | Assessment result/due | Optional | Assessment history | Competency | CBHRMS |
| Competency gap | GenerateCompetencyGap | CompetencyGapIdentified | Finalized -> Finalized | L&D | IDP prompt | Optional | Gap basis | Competency | CBHRMS/PRIME-HRM |
| IDP approval | ApproveIdp | IndividualDevelopmentPlanApproved | For Approval -> Approved | Competency, Reporting | IDP decision | Notify employee | IDP approval history | L&D | PRIME-HRM L&D |
| Performance rating | ValidatePerformanceRating | PerformanceRatingValidated | Under Review -> Finalized | Career, Rewards, L&D | Rating status | Optional | Rating snapshot | Performance | SPMS/PRIME-HRM |
| Training approval | ApproveLearningIntervention | LearningInterventionApproved | For Approval -> Approved | Notifications | L&D approval | Notify participant | Approval history | L&D | PRIME-HRM L&D |
| Leave application | SubmitLeaveApplication | LeaveApplicationSubmitted | Draft -> Submitted | Approver | Leave approval required | Notify approver | Submission audit | Leave | CSC leave |
| Leave approval | ApproveLeaveApplication | LeaveApplicationApproved | For Approval -> Approved | Attendance, Payroll prep | Leave decision | Side effects queued | Approval/ledger | Leave | CSC leave |
| Attendance correction | ApproveAttendanceAdjustment | AttendanceAdjustmentApproved | Under Review -> Approved | Payroll prep | Correction result | Side effects queued | Adjustment history | Attendance | Attendance rules |
| OB/travel | ApproveOfficialBusiness | OfficialBusinessApproved | For Approval -> Approved | Attendance | Approval decision | Notify employee | Approval history | Attendance | DepEd local rules |
| Service record | FinalizeServiceRecordUpdate | ServiceRecordUpdated | Under Review -> Released | Records, employee | Records task/result | Optional | Service history | Personnel Records | Records management |
| 201 document | VerifyEmployeeDocument | EmployeeDocumentVerified | Under Review -> Approved | Operational domains | Verification result | Optional | Verification/access log | Personnel Records | Records/privacy |
| Rewards | ApproveRecognition | RecognitionApproved | For Evaluation -> Approved | Records, Governance | Recognition result | Notify employee | Award history | Rewards | PRAISE |
| PRIME-HRM evidence | SubmitComplianceEvidence | ComplianceEvidenceSubmitted | Draft -> Submitted | Governance reviewer | Evidence due/received | Optional | Evidence history | Governance | PRIME-HRM |
| Policy activation | ApprovePolicyVersion | PolicyVersionApproved | For Approval -> Approved | All policy-driven domains | Policy update | Notify admins | Configuration history | Policy Configuration | DepEd/CSC/local |
| Access request | ApproveUserAccess | RoleAssigned | For Approval -> Finalized | Core Platform, Governance | Access/security alert | Optional | Permission audit | Core Platform | Data Privacy/security |
