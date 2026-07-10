# Document Matrix

## Purpose

Map representative HRIS document and record types to ownership, workflow, classification, verification, signature, versioning, retention, custody, viewers, and audit sensitivity.

| Document or record type | Owning domain | Related workflow | Structured data source | Classification | Verification required | Signature required | Versioned | Retention category | Primary custodian | Typical viewers | Audit sensitivity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Personal Data Sheet | Workforce | Onboarding/201 update | Employee profile | Confidential | Yes | No | Yes | Policy-configured | Records | Employee, HR | High |
| Work Experience Sheet | Workforce | Recruitment/career | Employee/applicant profile | Confidential | Yes | No | Yes | Policy-configured | Records | HR, evaluators | High |
| Eligibility certificate | Workforce/Recruitment | QS validation | Applicant/employee evidence | Confidential | Yes | No | Yes | Policy-configured | Records | HR, evaluator | High |
| Education credential | Workforce/Recruitment | QS validation | Applicant/employee evidence | Confidential | Yes | No | Yes | Policy-configured | Records | HR, evaluator | High |
| Training certificate | L&D | L&D/career/QS | Training participation | Confidential | Yes | No | Yes | Policy-configured | Records/L&D | Employee, HR | High |
| Vacancy publication | Recruitment | Vacancy publication | Vacancy | Public/Internal | Yes | As required | Yes | Policy-configured | HR | Applicants, HR | Medium |
| Applicant profile document | Recruitment | Application | Applicant | Applicant-Owned | Yes | No | Yes | Policy-configured | HR | Applicant, HR | High |
| Application letter | Recruitment | Application | Application | Applicant-Owned | Yes | No | Yes | Policy-configured | HR | Applicant, HR | High |
| Documentary checklist | Recruitment | Screening | Application | Internal | Yes | No | Yes | Policy-configured | HR | HR/evaluator | High |
| QS evidence packet | Recruitment | QS validation | Application/QS | HRMPSB Restricted | Yes | No | Yes | Policy-configured | HR | Evaluators, HRMPSB | Restricted |
| Screening result | Recruitment | Screening | Screening record | Confidential | Yes | No | Yes | Policy-configured | HR | Applicant, HR | High |
| Evaluation sheet | Recruitment | Comparative assessment | Evaluation | HRMPSB Restricted | Yes | Maybe | Yes | Policy-configured | HRMPSB secretariat | HRMPSB, auditors | Restricted |
| Interview record | Recruitment | Interview | Interview | HRMPSB Restricted | Yes | Maybe | Yes | Policy-configured | HRMPSB secretariat | HRMPSB | Restricted |
| HRMPSB conflict declaration | Recruitment | HRMPSB deliberation | HRMPSB governance | HRMPSB Restricted | Yes | Yes/acknowledge | Yes | Policy-configured | HRMPSB secretariat | HRMPSB, auditor | Restricted |
| Recusal record | Recruitment | HRMPSB deliberation | HRMPSB governance | HRMPSB Restricted | Yes | Maybe | Yes | Policy-configured | HRMPSB secretariat | HRMPSB, auditor | Restricted |
| Deliberation minutes/metadata | Recruitment | HRMPSB deliberation | HRMPSB record | HRMPSB Restricted | Yes | Maybe | Yes | Policy-configured | HRMPSB secretariat | HRMPSB, auditor | Restricted |
| Ranking report | Recruitment | Ranking | Ranking | HRMPSB Restricted/Internal | Yes | As required | Yes | Policy-configured | HR | HR, authority | Restricted |
| CAR/CAR-RQA/RQA-style output | Recruitment | Ranking/output | Assessment/ranking | Final Official Record | Yes | As required | Yes | Policy-configured | HR | Authorized recipients | Restricted |
| Appointment recommendation | Recruitment | Recommendation | Recommendation | Restricted Personnel Record | Yes | Yes/approval | Yes | Policy-configured | HR | Authority, HR | Restricted |
| Appointment form | Appointment | Appointment issuance | Appointment | Final Official Record | Yes | Yes | Yes | Policy-configured | Records | Employee, HR, CSC | Restricted |
| Position Description Form | Appointment/Plantilla | Appointment | Position profile | Confidential | Yes | As required | Yes | Policy-configured | Records | HR, CSC | High |
| Oath of Office | Appointment | Appointment | Appointment | Final Official Record | Yes | Yes | Yes | Policy-configured | Records | Employee, HR | High |
| Assumption to Duty | Appointment | Onboarding | Appointment/assignment | Final Official Record | Yes | Yes | Yes | Policy-configured | Records | Employee, HR | High |
| Medical certification | Appointment/Leave | Appointment/leave | Evidence | Highly Confidential | Yes | As required | Yes | Policy-configured | Records | Restricted HR | Restricted |
| Certification of publication | Appointment/Recruitment | Appointment | Publication | Final Official Record | Yes | Yes | Yes | Policy-configured | HR/Records | HR, CSC | High |
| CSC submission record | Appointment | CSC submission | CSC tracker | Restricted Personnel Record | Yes | No | Yes | Policy-configured | HR/Records | HR, auditor | Restricted |
| CSC action | Appointment | CSC action | CSC tracker | Restricted Personnel Record | Yes | No | Yes | Policy-configured | HR/Records | HR, employee if allowed | Restricted |
| Transfer order | Appointment | Personnel movement | Movement | Final Official Record | Yes | Yes | Yes | Policy-configured | Records | Employee, HR | High |
| Reassignment/detail document | Appointment | Personnel movement | Movement | Final Official Record | Yes | Yes | Yes | Policy-configured | Records | Employee, HR | High |
| Reclassification approval | Career Progression | Reclassification | Reclassification | Restricted Personnel Record | Yes | Yes | Yes | Policy-configured | Records | HR, employee if allowed | Restricted |
| Retitling/conversion record | Career Progression | Retitling/conversion | Career pathway | Restricted Personnel Record | Yes | Yes | Yes | Policy-configured | Records | HR, plantilla | Restricted |
| Performance plan | Performance | Performance cycle | Performance plan | Highly Confidential | Yes | No | Yes | Policy-configured | Performance HR | Employee, supervisor | Restricted |
| Validated rating | Performance | Rating validation | Rating snapshot | Highly Confidential | Yes | Maybe | Yes | Policy-configured | Performance HR | Employee, supervisor, authorized HR | Restricted |
| Competency assessment | Competency | Competency assessment | Assessment | Highly Confidential | Yes | No | Yes | Policy-configured | Competency HR | Employee, assessor, HR | Restricted |
| Competency evidence | Competency | Assessment/career | Evidence | Confidential/Restricted | Yes | No | Yes | Policy-configured | Records/Competency | Assessor, HR | High |
| Gap analysis | Competency | Gap/IDP | Gap record | Highly Confidential | Yes | No | Yes | Policy-configured | Competency HR | Employee, supervisor | Restricted |
| IDP | L&D | IDP approval | IDP | Confidential | Yes | Approval | Yes | Policy-configured | L&D HR | Employee, supervisor, HR | High |
| Training nomination | L&D | L&D request | L&D request | Internal/Confidential | Yes | Approval | Yes | Policy-configured | L&D HR | Employee, HR | High |
| Learning evaluation | L&D | Training completion | Evaluation | Confidential | Yes | No | Yes | Policy-configured | L&D HR | Employee, HR | High |
| Award nomination | Rewards | Recognition | Nomination | Confidential | Yes | No | Yes | Policy-configured | Rewards committee | Committee, HR | High |
| Recognition certificate | Rewards | Recognition | Recognition | Final Official Record | Yes | Maybe | Yes | Policy-configured | Records | Employee, HR | Medium |
| Leave application | Leave | Leave approval | Leave application | Confidential | Yes | Approval | Yes | Policy-configured | Leave HR | Employee, supervisor | High |
| Medical leave support | Leave | Leave approval | Evidence | Highly Confidential | Yes | No | Yes | Policy-configured | Records | Restricted HR | Restricted |
| Leave ledger | Leave | Leave ledger | Leave structured record | Restricted Personnel Record | Yes | No | Yes | Policy-configured | Leave HR | Employee, HR | Restricted |
| DTR | Attendance | DTR finalization | Attendance | Confidential | Yes | Maybe | Yes | Policy-configured | Attendance HR | Employee, HR | High |
| Attendance adjustment | Attendance | Correction | Adjustment | Confidential | Yes | Approval | Yes | Policy-configured | Attendance HR | Employee, supervisor | High |
| Travel order | Attendance | Travel approval | Travel/OB | Final Official Record | Yes | Yes | Yes | Policy-configured | Records/HR | Employee, HR | High |
| Payroll export | Payroll Preparation | Payroll prep | Payroll snapshot | Highly Confidential | Yes | No | Yes | Policy-configured | Payroll prep HR | Payroll authorized users | Restricted |
| Service record | Personnel Records | Service update/release | Service record | Final Official Record | Yes | Yes/certification | Yes | Policy-configured | Records | Employee, HR | Restricted |
| Document access log | Personnel Records | Access control | Access log | Restricted Personnel Record | System | No | Yes | Policy-configured | Records/Security | Auditor/security | Restricted |
| Policy issuance | Policy Configuration | Policy activation | Policy registry | Official Issuance | Yes | As source requires | Yes | Permanent/reference | Policy admin | HR, auditors | High |
| PRIME-HRM evidence summary | Governance | Compliance evidence | Evidence index | Confidential | Yes | Maybe | Yes | Policy-configured | Governance HR | PRIME-HRM focal, auditors | High |
| Audit report | Governance/Reporting | Audit | Audit logs | Highly Confidential | Yes | Maybe | Yes | Policy-configured | Auditor/Governance | Auditors, leadership | Restricted |
| Administrative case reference | Employee Relations | Discipline/grievance | Case reference | Restricted Personnel Record | Yes | As required | Yes | Policy-configured/hold | Restricted custodian | Authorized handlers only | Restricted |
