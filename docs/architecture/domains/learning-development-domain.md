# Learning and Development Domain

## Purpose

Own learning needs, IDPs, interventions, training programs, participation, evaluation, and development progress.

## Business Scope

Learning Need, Individual Development Plan, Learning Intervention, Training Program, Training Participation, Competency Gap Response, Training Evaluation, Development Progress.

## Out of Scope

Competency framework ownership, performance rating ownership, payroll, and appointment actions.

## Main Entities

Learning Need, Individual Development Plan, Learning Intervention, Training Program, Training Participation, Competency Gap Response, Training Evaluation, Development Progress.

## Aggregate or Ownership Candidates

Individual Development Plan, training program, training participation, development progress record.

## Key Business Rules

- This domain consumes competency gaps but owns learning plans and interventions.
- L&D outcomes may update development progress but do not automatically change competency assessments without assessment rules.
- Training evidence must remain linked to Personnel Records where documents exist.

## Commands or Use Cases

Create IDP, approve learning intervention, enroll participant, record completion, evaluate training, update development progress.

## Domain Events

IdpCreated, LearningInterventionApproved, TrainingParticipationRecorded, TrainingCompleted, DevelopmentProgressUpdated.

## Dependencies

Depends on Workforce, Competency, Performance, Policy and Configuration, Personnel Records, and Organization.

## Policy Dependencies

PRIME-HRM L&D, CBHRMS, DepEd professional development guidance, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log IDP approval, intervention changes, attendance/completion, evaluation, and development progress updates.

## Reports Produced

IDP status report, training needs analysis, L&D completion report, competency gap response report.

## Implementation Phase

Phase 6.
