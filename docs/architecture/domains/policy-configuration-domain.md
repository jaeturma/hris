# Policy and Configuration Domain

## Purpose

Own configurable policy rules, versions, effectivity, supersession, assessment frameworks, document sets, approval workflows, and local implementing memoranda.

## Business Scope

Policy Issuance, Policy Version, Effectivity Period, Supersession, Applicability Rule, Qualification Standard Version, Assessment Framework Version, Required Document Set, Approval Workflow Version, Merit Selection Plan Version, Competency Framework Version, Local Implementing Memorandum.

## Out of Scope

Operational record ownership, applicant evaluation execution, employee master data, and report generation.

## Main Entities

Policy Issuance, Policy Version, Effectivity Period, Supersession, Applicability Rule, Qualification Standard Version, Assessment Framework Version, Required Document Set, Approval Workflow Version, Merit Selection Plan Version, Competency Framework Version, Local Implementing Memorandum.

## Aggregate or Ownership Candidates

Policy issuance, policy version, assessment framework, QS version, approval workflow version, MSP version.

## Key Business Rules

- Do not hardcode scoring, qualification, documentary, or workflow rules directly into unrelated domains.
- National DepEd Orders, CSC issuances, Regional Memoranda, and Division Memoranda must be versioned and effectivity-bound.
- Local memoranda may implement or clarify but must not improperly override national policy.
- Completed workflows keep the policy and framework snapshots they used.

## Commands or Use Cases

Register policy issuance, approve policy version, define QS version, define assessment framework, publish document set, configure approval workflow, supersede policy.

## Domain Events

PolicyVersionApproved, AssessmentFrameworkPublished, QualificationStandardVersioned, ApprovalWorkflowVersioned, PolicySuperseded.

## Dependencies

Depends on Core Platform and Organization for actor and scope. Provides configuration to Recruitment, Appointment, Career Progression, Competency, Performance, L&D, Leave, Attendance, Governance, and Reporting.

## Policy Dependencies

DepEd Orders and Memoranda, CSC ORAOHRA, Agency Merit Selection Plan, PRIME-HRM, CBHRMS, Regional and Division Memoranda, Data Privacy Act, records management.

## Security Sensitivity

Restricted.

## Audit Requirements

Log creation, approval, amendment, supersession, effectivity changes, framework changes, and configuration exports.

## Reports Produced

Policy registry, effectivity calendar, supersession report, framework register, workflow configuration report.

## Implementation Phase

Phase 1 foundation before policy-driven modules.
