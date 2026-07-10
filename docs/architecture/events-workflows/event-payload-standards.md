# Event Payload Standards

## Purpose

Define safe, versioned, minimal event payloads.

## Required Payload Fields

| Field | Purpose |
| --- | --- |
| `event_id` | Unique event identifier. |
| `event_name` | Stable event name. |
| `schema_version` | Payload schema version. |
| `occurred_at` | Timestamp when fact happened. |
| `actor_id` | User or system actor reference. |
| `office_context` | Region, Division, District, School/IU, Office scope. |
| `aggregate_type` | Domain record type. |
| `aggregate_id` | Domain record identifier. |
| `workflow_id` | Workflow instance reference when applicable. |
| `policy_version_id` | Policy version reference when applicable. |
| `correlation_id` | Links related actions in a process. |
| `causation_id` | Event or command that caused this event. |
| `data` | Minimal business data. |
| `sensitivity` | Low, Medium, High, Restricted. |

## Rules

- Do not place full document contents in event payloads.
- Do not place unnecessary personal data in queued payloads.
- Use record references rather than duplicating sensitive records.
- Version event schemas.
- Preserve backward compatibility for integration events.
- Internal domain events may remain simpler than external integration events.

## Sensitive Data Rule

Restricted comments, deliberation details, medical details, discipline records, and document contents must stay in owning domain records and never travel in generic event payloads.
