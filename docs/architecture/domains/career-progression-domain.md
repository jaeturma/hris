# Career Progression Domain

## Purpose

Own career pathways that are not generic recruitment, including higher teaching position applications, expanded career progression, reclassification, retitling, conversion, Master Teacher progression, and School Principal progression.

## Business Scope

Higher Teaching Position Application, Expanded Career Progression, Reclassification, Retitling, Career Stage, Promotion Path, Master Teacher Progression, School Principal Progression, Career Readiness, Supporting Evidence, and Approval History.

## Out of Scope

Open-vacancy recruitment cycles, appointment issuance, leave, attendance, and general employee master data.

## Main Entities

Career Pathway, Higher Teaching Position Application, Reclassification Request, Retitling Request, Career Stage, Promotion Path, Master Teacher Progression, School Principal Progression, Career Readiness, Supporting Evidence, Approval History.

## Aggregate or Ownership Candidates

Career progression application, pathway record, reclassification request, retitling/conversion record, readiness assessment.

## Key Business Rules

- Do not merge all career actions into one promotion process.
- Every pathway must reference policy version, assessment framework, QS version, competency framework, and effectivity period.
- Historical performance and competency snapshots must be preserved.
- Approved actions may trigger Appointment and Personnel Action, Plantilla, Personnel Records, and Service Record updates.

## Commands or Use Cases

Submit higher teaching application, assess career readiness, request reclassification, request retitling, finalize Master Teacher progression, finalize School Principal progression.

## Domain Events

CareerPathwayOpened, CareerEvidenceSubmitted, CareerAssessmentFinalized, ReclassificationApproved, RetitlingApproved, CareerProgressionRecommended.

## Dependencies

Depends on Workforce, Plantilla and Position, Competency, Performance, Learning and Development, Policy and Configuration, HRMPSB governance via Recruitment/Policy records, and Personnel Records.

## Policy Dependencies

DepEd higher teaching, expanded career progression, reclassification, amendments and clarifications, CSC ORAOHRA, PRIME-HRM, CBHRMS, Regional and Division Memoranda.

## Security Sensitivity

High.

## Audit Requirements

Log pathway classification, evidence changes, evaluation snapshots, HRMPSB actions, recommendations, approvals, denials, and downstream action triggers.

## Reports Produced

Career progression pipeline, Master Teacher progression report, School Principal progression report, reclassification tracker, retitling/conversion tracker, readiness report.

## Implementation Phase

Phase 7 after Workforce, Plantilla, Competency, Performance, Policy, and Personnel Records.
