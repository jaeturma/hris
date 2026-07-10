# Organization Domain

## Purpose

Own the DepEd organizational structure and data scope used by every HR process.

## Business Scope

Region, Division, District, School, Implementing Unit, Office, Office Unit, Section, Station, organizational hierarchy, office context, and data scope.

## Out of Scope

Employee employment records, plantilla occupancy, user role assignment, and recruitment cycles.

## Main Entities

Region, Division, District, School, Implementing Unit, Office, Office Unit, Section, Station, Organizational Hierarchy, Office Context, Data Scope.

## Aggregate or Ownership Candidates

Office hierarchy, station, office unit, data scope rule.

## Key Business Rules

- Never assume one office.
- Office hierarchy controls visibility, ownership, reporting scope, and approval context.
- Schools and Implementing Units may have different operational capabilities.
- Other domains reference offices but must not redefine office hierarchy.

## Commands or Use Cases

Create office, update hierarchy, assign station, configure office scope, deactivate office unit.

## Domain Events

OfficeCreated, OfficeHierarchyChanged, StationRegistered, OfficeScopeChanged.

## Dependencies

Depends on Core Platform for audit actors. Provides scope to nearly all domains.

## Policy Dependencies

DepEd governance structure, Regional and Division Memoranda, Data Privacy scope rules.

## Security Sensitivity

Medium.

## Audit Requirements

Log hierarchy changes, station changes, office activation/deactivation, and scope rule changes.

## Reports Produced

Office hierarchy report, station list, school/IU directory, scope coverage report.

## Implementation Phase

Phase 1 foundation.
