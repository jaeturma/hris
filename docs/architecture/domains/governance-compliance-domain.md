# Governance and Compliance Domain

## Purpose

Own PRIME-HRM readiness, compliance evidence, audit findings, corrective actions, retention rules, privacy reviews, segregation of duties, and access reviews.

## Business Scope

PRIME-HRM Readiness, Compliance Requirement, Compliance Evidence, Audit Finding, Corrective Action, Records Retention Rule, Data Privacy Review, Segregation of Duties, Access Review.

## Out of Scope

Operational source records, report generation ownership, user authentication, and domain-specific decisions.

## Main Entities

PRIME-HRM Readiness, Compliance Requirement, Compliance Evidence, Audit Finding, Corrective Action, Records Retention Rule, Data Privacy Review, Segregation of Duties Rule, Access Review.

## Aggregate or Ownership Candidates

Compliance requirement, audit finding, corrective action, access review.

## Key Business Rules

- Governance may reference evidence across domains but must not rewrite source records.
- PRIME-HRM evidence must preserve source, owner, policy version, and sensitivity.
- Access reviews and segregation-of-duties checks must be auditable.

## Commands or Use Cases

Register compliance requirement, attach evidence reference, record audit finding, assign corrective action, conduct access review.

## Domain Events

ComplianceRequirementRegistered, EvidenceLinked, AuditFindingRecorded, CorrectiveActionAssigned, AccessReviewCompleted.

## Dependencies

Depends on all operational domains for evidence references, Core Platform for access data, and Policy and Configuration for requirements.

## Policy Dependencies

CSC PRIME-HRM, Data Privacy Act, government records management, DepEd compliance requirements, audit standards.

## Security Sensitivity

Restricted.

## Audit Requirements

Log evidence linking, findings, corrective actions, privacy reviews, access reviews, and exports.

## Reports Produced

PRIME-HRM readiness report, compliance dashboard, audit finding register, corrective action tracker, access review report.

## Implementation Phase

Phase 10, with early design in Phase 1.
