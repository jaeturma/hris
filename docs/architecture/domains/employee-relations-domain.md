# Employee Relations Domain

## Purpose

Own restricted employee-relations records such as grievances, complaints, discipline references, incidents, resolutions, and appeal history.

## Business Scope

Grievance, Complaint, Administrative Case Reference, Discipline, Incident, Resolution, Restricted Access, Appeal History.

## Out of Scope

General performance management, leave approvals, appointment decisions, and legal adjudication outside HRIS records support.

## Main Entities

Grievance, Complaint, Administrative Case Reference, Discipline Record, Incident, Resolution, Restricted Access Record, Appeal History.

## Aggregate or Ownership Candidates

Restricted employee-relations case, incident record, grievance record.

## Key Business Rules

- This domain is highly sensitive and may be deferred pending policy validation.
- Access must be narrower than ordinary HR access.
- HRIS records support documentation and routing; they do not make legal conclusions.

## Commands or Use Cases

Register grievance, record incident, restrict case access, update resolution, record appeal history.

## Domain Events

GrievanceRegistered, IncidentRecorded, CaseAccessRestricted, ResolutionRecorded, AppealRecorded.

## Dependencies

Depends on Workforce, Organization, Core Platform, Policy and Configuration, Personnel Records, and Governance.

## Policy Dependencies

CSC rules, DepEd administrative and grievance procedures, Data Privacy Act, records management.

## Security Sensitivity

Restricted.

## Audit Requirements

Log every create, view, update, export, access grant, access revocation, and status change.

## Reports Produced

Restricted case register, case status report, action timeline, access review report.

## Implementation Phase

Later phase; defer until HR/legal validation.
