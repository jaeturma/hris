# 201 File Architecture

## Purpose

Define the employee 201 File as a controlled records collection, not merely one folder.

## Architecture Rules

- The 201 File is an indexed collection of structured references, document metadata, versions, verification records, access logs, and retention statuses.
- Structured data owners remain separate from document owners.
- Highly sensitive administrative, medical, grievance, or disciplinary records must not be exposed through ordinary 201 File access.
- Employee self-service access must be limited to allowed own-record copies.

## 201 File Categories

| Category | Structured data owner | Document owner | Required metadata | Versioning | Verification | Access level | Retention | Expiry / reminders | Reporting use |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Personal Data Sheet | Workforce | Personnel Records | employee, date received, version. | Yes | Human/metadata. | High | Policy-configured. | When updated. | Employee profile evidence. |
| Work Experience Sheet | Workforce | Personnel Records | employee, date, source. | Yes | Human. | High | Policy-configured. | As updated. | QS/promotion evidence. |
| Eligibility | Workforce/Recruitment | Personnel Records | eligibility type, issued date, expiry if any. | Yes | Authenticity/expiry. | High | Policy-configured. | If expiring. | QS evidence. |
| Education | Workforce/Recruitment | Personnel Records | school, degree, date. | Yes | Human/authenticity. | High | Policy-configured. | None unless credential expiry exists. | QS evidence. |
| Training | L&D | Personnel Records | provider, hours, date, certificate. | Yes | Human/metadata. | High | Policy-configured. | Expiring certification. | L&D and QS evidence. |
| Appointment | Appointment | Personnel Records | appointment id, item, effective date. | Yes | Records validation. | Restricted | Policy-configured/permanent if required. | None. | Appointment/service evidence. |
| Assumption | Appointment | Personnel Records | assumption date, office. | Yes | Records validation. | High | Policy-configured. | None. | Onboarding/service. |
| Oath | Appointment | Personnel Records | date, signatory, office. | Yes | Signature/human. | High | Policy-configured. | None. | Appointment evidence. |
| Medical | Workforce/Leave as applicable | Personnel Records | document type, date, sensitivity. | Yes | Restricted verification. | Restricted | Policy-configured. | Expiry where applicable. | Limited, not ordinary 201 view. |
| Clearances | Recruitment/Appointment | Personnel Records | clearance type, issued date, expiry. | Yes | Authenticity/expiry. | Restricted/High | Policy-configured. | Expiry reminders. | Appointment compliance. |
| Service Record | Personnel Records | Personnel Records | generated date, source snapshot. | Yes | Records certification. | High | Policy-configured. | When action changes. | Service history. |
| Performance Ratings | Performance | Personnel Records | cycle, rating snapshot, validation date. | Yes | Performance validation. | Restricted | Policy-configured. | Cycle reminders. | Promotion/performance evidence. |
| Leave Records | Leave | Personnel Records | leave application/ledger refs. | Yes | HR validation. | High/Restricted | Policy-configured. | Balance/cutoff as needed. | Leave reports. |
| Personnel Movements | Appointment | Personnel Records | movement type, effective date. | Yes | Records validation. | High | Policy-configured. | None. | Service record. |
| Awards and Recognition | Rewards | Personnel Records | award, program, date. | Yes | HR/committee validation. | High | Policy-configured. | None. | PRIME-HRM/R&R. |
| Learning and Development | L&D | Personnel Records | program, completion, evaluation. | Yes | L&D validation. | High | Policy-configured. | Expiring certs. | L&D/IDP. |
| Competency Assessments | Competency | Personnel Records | framework, assessment id, evidence. | Yes | Assessor validation. | Restricted/High | Policy-configured. | Assessment cycles. | CBHRMS evidence. |
| SALN references | Workforce/Compliance | Personnel Records | year, submission status. | Yes | Restricted validation. | Restricted | Policy-configured. | Annual cycle. | Compliance only. |
| Administrative records | Employee Relations | Restricted Records Custodian | case ref, status, hold. | Yes | Restricted process. | Restricted | Policy-configured/hold. | Case-dependent. | Restricted reports only. |
| Separation or retirement | Appointment/Workforce | Personnel Records | separation type, effective date. | Yes | Records validation. | High | Policy-configured. | Retirement forecast. | Lifecycle closure. |
