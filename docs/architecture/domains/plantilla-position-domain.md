# Plantilla and Position Domain

## Purpose

Own official plantilla, item, position, vacancy, salary, and position profile records.

## Business Scope

Plantilla Item, Item Number, Position Title, Salary Grade, Position Level, Position Classification, Occupancy, Vacancy Status, Qualification Standard Reference, and Position Profile.

## Out of Scope

Employee identity, recruitment applications, appointment documents, competency dictionary ownership, and payroll disbursement.

## Main Entities

Plantilla Item, Item Number, Position Title, Salary Grade, Position Level, Position Classification, Occupancy, Vacancy Status, Qualification Standard Reference, Position Profile.

## Aggregate or Ownership Candidates

Plantilla item, position title, position profile, occupancy record.

## Key Business Rules

- Position title is the authorized title.
- Plantilla item is the funded/authorized item with item number.
- Occupant is the employee encumbering the item.
- Assignment is where the employee serves.
- Vacancy is a status or event derived from item and occupancy conditions.

## Commands or Use Cases

Create plantilla item, update position profile, mark item vacant, encumber item, release item, update salary grade reference.

## Domain Events

PlantillaItemCreated, ItemVacated, ItemEncumbered, PositionProfileUpdated, VacancyStatusChanged.

## Dependencies

Depends on Organization, Policy and Configuration, Competency, and Workforce for occupancy references. Provides item and position data to Recruitment, Appointment, Career Progression, and Reporting.

## Policy Dependencies

DepEd plantilla and staffing guidance, CSC Qualification Standards, salary grade references, records management.

## Security Sensitivity

High.

## Audit Requirements

Log item number changes, vacancy status changes, encumbrance changes, salary grade changes, and position profile version changes.

## Reports Produced

Plantilla masterlist, vacant item list, encumbered item report, position profile report, salary grade summary.

## Implementation Phase

Phase 2.
