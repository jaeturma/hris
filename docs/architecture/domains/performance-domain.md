# Performance Domain

## Purpose

Own performance cycles, plans, ratings, rating evidence, validated rating snapshots, and performance history.

## Business Scope

Performance Cycle, Performance Plan, Performance Commitment, Performance Rating, Validated Rating, Rating Evidence, Performance History, Promotion Eligibility Reference.

## Out of Scope

Competency dictionary ownership, L&D intervention ownership, rewards decisions, and career progression final approval.

## Main Entities

Performance Cycle, Performance Plan, Performance Commitment, Performance Rating, Validated Rating, Rating Evidence, Performance History, Promotion Eligibility Reference.

## Aggregate or Ownership Candidates

Performance cycle, employee performance record, validated rating snapshot.

## Key Business Rules

- Performance ratings used by other workflows must be versioned snapshots.
- Corrections create new versions and do not silently rewrite completed evaluations.
- Integration with Competency, Career Progression, and Rewards must preserve the rating version used.

## Commands or Use Cases

Open performance cycle, submit performance plan, record rating, validate rating, correct rating, publish rating snapshot.

## Domain Events

PerformanceCycleOpened, PerformancePlanSubmitted, PerformanceRatingRecorded, PerformanceRatingValidated, PerformanceSnapshotCreated.

## Dependencies

Depends on Workforce, Organization, Policy and Configuration, Competency, and Personnel Records. Feeds Career Progression, L&D, Rewards, Governance, and Reporting.

## Policy Dependencies

SPMS-related requirements, CSC rules, PRIME-HRM Performance Management, DepEd performance guidance, Data Privacy Act.

## Security Sensitivity

Restricted.

## Audit Requirements

Log rating submission, validation, correction, snapshot creation, access, and use in downstream workflows.

## Reports Produced

Performance cycle report, rating distribution, pending ratings, promotion eligibility reference, competency-performance linkage report.

## Implementation Phase

Phase 5.
