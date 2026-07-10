# Implementation Boundaries

## Purpose

Recommend future Laravel and React organization that follows the enterprise domain model without creating code folders during this documentation phase.

## Laravel Organization Recommendation

When code implementation begins, consider a practical domain-oriented structure:

```text
app/
  Domains/
    Organization/
    Workforce/
    Plantilla/
    Recruitment/
    Appointment/
    CareerProgression/
    Competency/
    Performance/
    LearningDevelopment/
    PersonnelRecords/
    Leave/
    Attendance/
    PayrollPreparation/
    RewardsRecognition/
    EmployeeRelations/
    Governance/
    Reporting/
    Integration/
    PolicyConfiguration/
```

Each domain may eventually contain only the folders it needs:

```text
Actions/
Data/
Enums/
Events/
Models/
Policies/
Queries/
Services/
Support/
```

Do not force every domain to contain every folder. Do not create folders until implementation requires them.

## React Organization Recommendation

When frontend implementation begins, align feature folders with domain boundaries where practical:

```text
resources/js/
  features/
    organization/
    workforce/
    plantilla/
    recruitment/
    appointment/
    career-progression/
    competency/
    performance/
    learning-development/
    personnel-records/
    leave/
    attendance/
    payroll-preparation/
    governance/
    reporting/
    system-administration/
```

React features should not bypass server-side authorization, policy configuration, or domain services. Inertia pages should present domain workflows, not own business rules.

## Implementation Rules

- Start with Core Platform, Organization, Policy and Configuration, Workforce, and Plantilla foundations.
- Define permissions, office scope, audit events, and policy versions before workflow code.
- Keep domain writes inside the owning domain.
- Use application actions or services for cross-domain orchestration.
- Use events for downstream reactions when immediate synchronous updates are not required.
- Use reporting projections for analytics instead of operational writes.
- Keep integrations at boundaries and route imported data through domain commands.

## Practical Non-Overengineering Rule

Use domain organization to reduce coupling and improve clarity. Do not introduce complex DDD patterns, repositories, event sourcing, or service layers unless they solve an immediate project problem.

## Recommended Phase Sequencing

| Phase | Domains |
| --- | --- |
| Phase 1 | Core Platform, Organization, Policy and Configuration, Workforce foundation |
| Phase 2 | Plantilla and Position, Competency foundation |
| Phase 3 | Personnel Records, employee 201 file foundation |
| Phase 4 | Recruitment and Selection, Appointment foundation |
| Phase 5 | Performance, competency assessment linkage |
| Phase 6 | Learning and Development |
| Phase 7 | Career Progression, reclassification, retitling/conversion pathways |
| Phase 8 | Rewards and Recognition |
| Phase 9 | Leave, Attendance, Payroll Preparation |
| Phase 10 | Governance, Reporting, Analytics, Integration, AI assistance |

## Boundaries That Must Not Be Crossed

- Controllers must not hardcode policy criteria.
- React pages must not compute official scores, rankings, leave balances, or appointment eligibility.
- Reports must not update source data.
- Integrations must not bypass domain validation.
- Uploaded documents must not replace structured records.
- AI assistance must not make final HR decisions.
