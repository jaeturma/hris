# Domain Ownership Matrix

## Purpose

Identify the owning domain, read access, write authority, policy source, and audit sensitivity for core HRIS concepts.

| Entity or Concept | Owning Domain | Read Access by Other Domains | Write Authority | Policy Source | Audit Sensitivity |
| --- | --- | --- | --- | --- | --- |
| Employee | Workforce | Most HR domains by office scope | Workforce only, with appointment/personnel-action triggers | CSC personnel rules, DepEd personnel administration | High |
| User | Core Platform | All domains for actor references | Core Platform administrators | Access governance, Data Privacy | Restricted |
| Office | Organization | All domains | Organization administrators | DepEd hierarchy, local office structure | Medium |
| Plantilla Item | Plantilla and Position | Workforce, Recruitment, Appointment, Career, Payroll, Reporting | Plantilla and Position | DepEd plantilla rules, CSC QS references | High |
| Vacancy | Recruitment and Selection | Plantilla, Appointment, Reporting | Recruitment and Selection | DepEd hiring issuances, MSP | High |
| Application | Recruitment and Selection | HRMPSB, Appointment, Reporting, Governance | Recruitment and Selection | DepEd hiring issuances, Data Privacy | High |
| Appointment | Appointment and Personnel Action | Workforce, Plantilla, Personnel Records, Payroll, Reporting | Appointment and Personnel Action | CSC ORAOHRA, DepEd appointment rules | Restricted |
| Personnel Movement | Appointment and Personnel Action | Workforce, Plantilla, Attendance, Payroll, Records, Reporting | Appointment and Personnel Action | DepEd personnel action guidance, CSC rules | High |
| Competency | Competency | Recruitment, Career, Performance, L&D, Rewards, Reporting | Competency | PRIME-HRM, CBHRMS, DepEd competency guidance | High |
| Performance Rating | Performance | Career, L&D, Rewards, Governance, Reporting by permission | Performance | SPMS-related guidance, PRIME-HRM | Restricted |
| Individual Development Plan | Learning and Development | Competency, Performance, Career, Reporting by permission | Learning and Development | PRIME-HRM L&D, CBHRMS | High |
| Employee Document | Personnel Records | Operational domains by evidence reference | Personnel Records | Records management, Data Privacy, DepEd records rules | Restricted |
| Leave Credit | Leave | Attendance, Payroll, Reporting by permission | Leave | CSC leave rules, DepEd leave administration | High |
| Attendance Log | Attendance | Leave, Payroll, Reporting by permission | Attendance | Attendance rules, local procedures | High |
| Payroll Preparation Record | Payroll Preparation | Workforce, Reporting, Governance by permission | Payroll Preparation | Payroll preparation controls, Data Privacy | Restricted |
| Policy Version | Policy and Configuration | All policy-driven domains | Policy and Configuration after HR/legal approval | DepEd, CSC, Regional/Division Memoranda | High |
| Audit Log | Core Platform | Governance, Reporting, authorized auditors | System/Core Platform only | Audit requirements, Data Privacy | Restricted |
| Recruitment Cycle | Recruitment and Selection | Appointment, Governance, Reporting | Recruitment and Selection | DepEd hiring rules, MSP | High |
| HRMPSB Constitution | Policy and Configuration / Recruitment Governance | Recruitment, Career, Governance | Policy and Configuration with HR owner approval | CSC ORAOHRA, MSP, DepEd guidance | Restricted |
| Assessment Framework | Policy and Configuration | Recruitment, Career, Competency, Reporting | Policy and Configuration | DepEd issuances, CSC rules, local memoranda | High |
| CSC Submission | Appointment and Personnel Action | Workforce, Records, Governance, Reporting | Appointment and Personnel Action | CSC ORAOHRA | Restricted |
| Reclassification Request | Career Progression | Appointment, Plantilla, Records, Reporting | Career Progression | DepEd career/reclassification rules, CSC rules | High |
| 201 File | Personnel Records | Workforce, Appointment, Governance by permission | Personnel Records | Records management, Data Privacy | Restricted |

## Ownership Rules

- Read access is not write authority.
- Policy source does not imply policy interpretation by the operational domain.
- Sensitive cross-domain reads must include office scope, permission, purpose, and audit trail.
- Report snapshots must identify source domain and extraction time.
