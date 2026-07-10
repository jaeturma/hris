# Workflow Engine

## Purpose

Define a configurable workflow engine that supports DepEd HR workflows without becoming so abstract that HR staff cannot understand or maintain it.

## Conceptual Records

| Conceptual Record | Purpose |
| --- | --- |
| `workflow_definitions` | Human-readable workflow family such as Leave Approval or HRMPSB Deliberation. |
| `workflow_definition_versions` | Versioned workflow rules with effective dates and policy references. |
| `workflow_steps` | Named steps using domain language. |
| `workflow_transitions` | Allowed movement between states or steps. |
| `workflow_conditions` | Policy-configured guards and branches. |
| `workflow_instances` | A running workflow for one record or cycle. |
| `workflow_step_instances` | Runtime step records. |
| `workflow_assignments` | User, role, office, HRMPSB, evaluator, or delegated assignments. |
| `workflow_actions` | Submitted, approved, returned, rejected, cancelled, reopened, or finalized actions. |
| `workflow_deadlines` | Policy, service-level, reminder, or regulatory deadlines. |
| `workflow_escalations` | Escalation history and reassignment records. |
| `workflow_snapshots` | Frozen policy, workflow, evidence, and actor context. |

Do not create migrations from this list yet.

## Generic Concepts

Workflow definition, version, step, transition, condition, assignment, action, deadline, escalation, snapshot, and history can be generic.

## Domain-Specific Concepts

Vacancy, application, HRMPSB deliberation, appointment, CSC action, career progression pathway, reclassification, competency assessment, performance rating, leave application, DTR, service record, and 201 file document must remain domain-specific.

## Required Capabilities

- Workflow definition versions and effective dates.
- Policy references and office applicability.
- Position applicability and pathway applicability.
- Role-based, user-specific, office-scoped, evaluator, and HRMPSB assignments.
- Conditional branches and required documents.
- Return for compliance, rejection, cancellation, reopening, escalation, deadline tracking, finalization, snapshots, and history.

## Maintainability Rule

Use domain labels in workflow definitions. HR staff should see "For HRMPSB Deliberation" or "Returned for Documentary Compliance," not abstract machine names.

## Policy Rule

Active workflows preserve their starting policy and workflow definition versions unless an authorized transition or migration rule explicitly applies.
