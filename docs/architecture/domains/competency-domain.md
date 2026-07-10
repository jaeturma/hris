# Competency Domain

## Purpose

Own competency frameworks, dictionaries, position competency profiles, assessments, evidence, gaps, and historical competency records.

## Business Scope

Competency Model, Competency Dictionary, Core Competency, Leadership Competency, Technical Competency, Job Family, Proficiency Level, Behavioral Indicator, Position Competency Profile, Competency Assessment, Competency Gap, Competency Evidence.

## Out of Scope

Learning intervention ownership, performance rating ownership, appointment decisions, and recruitment scoring ownership.

## Main Entities

Competency Model, Competency, Competency Category, Job Family, Proficiency Level, Behavioral Indicator, Position Competency Profile, Competency Assessment, Competency Gap, Competency Evidence.

## Aggregate or Ownership Candidates

Competency framework, competency dictionary, position competency profile, competency assessment, competency gap analysis.

## Key Business Rules

- Competency records must be versioned and historical.
- Position competency profiles reference Plantilla/Position but own competency requirements.
- Assessment evidence must cite method, assessor, framework version, and date.
- Later framework changes must not rewrite completed assessments.

## Commands or Use Cases

Create competency model, approve dictionary version, map position competencies, assess competency, generate gap analysis.

## Domain Events

CompetencyModelApproved, PositionCompetencyProfileUpdated, CompetencyAssessed, CompetencyGapIdentified.

## Dependencies

Depends on Policy and Configuration, Plantilla and Position, Workforce, Performance, and Personnel Records evidence references. Feeds Recruitment, Career Progression, Learning and Development, Rewards, and Reporting.

## Policy Dependencies

CSC PRIME-HRM, CSC CBHRMS, DepEd competency guidance, position profile governance, Data Privacy Act.

## Security Sensitivity

High.

## Audit Requirements

Log model approval, profile changes, assessment creation, evidence changes, gap generation, and assessor actions.

## Reports Produced

Competency dictionary, position competency matrix, assessment report, competency gap report, succession readiness report.

## Implementation Phase

Phase 2 foundation with Plantilla and Position.
