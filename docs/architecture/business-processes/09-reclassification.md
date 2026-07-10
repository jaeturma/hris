# 09 Reclassification

## Purpose

Manage reclassification requests with complete evidence, position and plantilla validation, competency linkage, approval routing, and records updates.

Reclassification must be separated into standard reclassification, expanded reclassification under career progression, retitling, and position conversion where those actions have different legal, plantilla, assessment, and records consequences.

## Trigger

Employee or office request, career progression event, position duty change, policy-directed reclassification window, or HR planning need.

## Actors

Employee, school or office head, HR officer, plantilla manager, evaluator, approving authority, records officer, auditor.

## Inputs

Reclassification request, position and plantilla data, service record, performance ratings, competency evidence, job duties, supporting documents, and approval path.

Required governance inputs include reclassification policy version, pathway type, plantilla action type, qualification-standard version, competency-framework version, assessment-framework version where applicable, transitory rule, and effectivity period.

## High-Level Process Flow

1. Submit or initiate reclassification request.
2. Classify as standard reclassification, expanded reclassification, retitling, position conversion, or related action.
3. Validate employee, position, item, office, and documentary requirements.
4. Freeze current employee, item, position, performance, competency, and document snapshots.
5. Review qualification, performance, duty, and competency evidence using the applicable versioned framework.
6. Route through required evaluators, HRMPSB where required, and approval authorities.
7. Record approval, denial, deferral, returned status, or transition handling.
8. Update plantilla, position, employee assignment, service record, and 201 file as applicable.

## Decision Points

- Is the request within an allowed reclassification basis?
- Is the action expanded reclassification, retitling, position conversion, or another personnel action?
- Is the item and position data valid?
- Are qualification, competency, performance, and document requirements complete?
- Does approval cause position, salary grade, or service record changes?
- Which effectivity date, superseded policy, and transitory provision applies?

## Outputs

Reclassification request record, evidence checklist, evaluation result, approval history, updated item or employee records, reportable decision.

## Applicable Policy Area

DepEd reclassification guidance and memoranda; career progression issuances; CSC rules; records management; Data Privacy Act.

## PRIME-HRM Contribution

Supports Recruitment/Placement, Performance Management, L&D, and rewards-related career evidence.

## Competency-Based HRM Link

Uses required competencies, demonstrated competencies, gap analysis, promotion readiness, and succession readiness where applicable.

## System Responsibilities

Track request states, evidence, decisions, related documents, item impacts, service record impacts, and audit history.

The system must maintain separate action types for reclassification, expanded reclassification, retitling, and position conversion. It must also preserve immutable snapshots, versioned policy references, versioned assessment or competency frameworks, approval histories, item impacts, salary-grade impacts, position-title impacts, CSC submission or validation steps where applicable, and service-record consequences.

## Workflow Boundary

- Expanded reclassification belongs to the career progression pathway when the verified policy basis says so.
- Retitling or position conversion must not be recorded as promotion unless the verified policy basis requires it.
- Ordinary transfer, reassignment, detail, or station movement must remain under personnel movement.
- Open-vacancy appointment must remain under recruitment, selection, and appointment.

## Manual Validation Flags

- Validate exact reclassification, expanded reclassification, retitling, and conversion rules before implementation.
- Validate whether a CSC action, appointment, notice, or submission lifecycle is required for each action type.

## Automation Opportunity Rating

Medium - workflow routing and evidence checks are automatable, but eligibility logic needs careful local policy validation.

## AI Readiness Rating

Medium - AI can summarize evidence and identify missing documents, but reclassification decisions must remain human and policy-driven.

## AI Opportunities

Evidence packet summary, missing support detection, comparison of current and target profile, and draft status explanation.

## Reports Produced

Reclassification request list, pending approvals, approved actions, denied or returned requests, item impact report.

## Security Considerations

Restrict salary, performance, competency, and decision records; log every document access and status change.

## Future Integrations

Document Management, Payroll, Digital Signature, Email, Government Portals, AI Assistant.

## Related Business Processes

Career Progression, Plantilla Management, Personnel Movement, Service Record Management, 201 Files Management.
