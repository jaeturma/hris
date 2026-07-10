# Recruitment and Selection Domain

## Purpose

Own vacancy-to-recommendation workflows for open-vacancy appointment and DepEd hiring/selection cycles.

## Business Scope

Recruitment Cycle, Vacancy, Publication, Applicant, Application, Documentary Requirement, Screening, Evaluation, Comparative Assessment, Interview, Ranking, HRMPSB Deliberation, and Recommendation.

## Out of Scope

Appointment issuance, CSC submission, employee onboarding, internal personnel movement, career progression pathways, and final employee master record creation.

## Main Entities

Recruitment Cycle, Vacancy, Publication, Applicant, Application, Documentary Requirement, Screening Result, Evaluation, Comparative Assessment, Interview, Ranking, HRMPSB Deliberation, Recommendation.

## Aggregate or Ownership Candidates

Recruitment cycle, vacancy, applicant, application, assessment record, HRMPSB recommendation.

## Key Business Rules

- Align primarily with applicable DepEd hiring and selection issuances.
- Assessment frameworks must be policy-versioned and effectivity-bound.
- Completed evaluations must preserve immutable snapshots.
- HRMPSB membership is cycle-specific or constitution-specific, not only a user role.
- Recruitment recommendation does not equal appointment.

## Commands or Use Cases

Open recruitment cycle, publish vacancy, register applicant, submit application, verify documents, finalize evaluation, record HRMPSB recommendation.

## Domain Events

VacancyPublished, ApplicantRegistered, ApplicationSubmitted, ScreeningCompleted, EvaluationFinalized, RankingGenerated, RecommendationIssued.

## Dependencies

Depends on Organization, Plantilla and Position, Policy and Configuration, Competency, Core Platform, and Personnel Records document references. Feeds Appointment and Personnel Action.

## Policy Dependencies

DepEd hiring and selection issuances, CSC ORAOHRA, Agency Merit Selection Plan, HRMPSB rules, Regional and Division Memoranda, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log publication, application submission, document verification, evaluator actions, score changes, ranking generation, HRMPSB deliberation metadata, recusals, and recommendations.

## Reports Produced

Vacancy report, applicant list, qualified applicant list, evaluation report, ranking report, CAR/CAR-RQA/RQA-style outputs where applicable, recommendation report.

## Implementation Phase

Phase 4 after Policy, Organization, Plantilla, Competency, and Personnel Records foundations.
