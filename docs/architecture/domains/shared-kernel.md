# Shared Kernel

## Purpose

Define the smallest set of shared concepts that may be referenced across domains without creating a large shared model layer.

## Shared Concepts

| Concept | Use |
| --- | --- |
| Office identifier | Scopes records to Region, Division, District, School, IU, Office, Unit, or Station. |
| Employee identifier | References workforce identity without copying employee business rules. |
| User identifier | References authenticated user and actor context. |
| Money value | Salary, allowance, deduction, and payroll preparation values. |
| Date range | Effectivity periods, appointments, cycles, and validity windows. |
| Document reference | Points to evidence without giving ownership to operational domains. |
| Policy reference | Links records to policy version, effectivity, and supersession. |
| Status history | Common status timeline pattern for workflow records. |
| Approval reference | Links to approval flow, step, action, and actor metadata. |
| Audit metadata | Actor, timestamp, office context, IP/device where applicable, and event name. |

## Out of Scope

The shared kernel must not contain large models such as Employee, Plantilla Item, Application, Appointment, Leave Application, Competency Assessment, or Performance Rating. It must not contain DepEd policy logic.

## Key Business Rules

- Shared references can identify a record but must not allow direct writes across domain boundaries.
- Shared value objects should be boring, stable, and policy-neutral.
- If a concept has meaningful HR rules, it belongs in a domain, not the shared kernel.

## Audit Requirements

Shared metadata must support immutable history, office scope, actor traceability, and later reporting.

## Implementation Phase

Phase 1 foundation, as reusable conventions only. Avoid creating shared abstractions before code actually needs them.
