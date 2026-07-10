# Idempotency and Retries

## Purpose

Prevent duplicate approvals, duplicate personnel actions, repeated notifications, duplicate imports, and duplicate exports during retries or repeated submissions.

## Recommended Identifiers

`event_id`, `workflow_action_id`, `external_reference`, `idempotency_key`, `import_batch_id`, `notification_delivery_id`, `export_batch_id`, `digital_signature_request_id`.

## Standards

| Scenario | Idempotency Rule |
| --- | --- |
| Duplicate event handling | Store processed `event_id` or aggregate/version pair. |
| Duplicate job execution | Use job-specific idempotency key. |
| Repeated webhook delivery | Use `external_reference` and provider event ID. |
| Repeated imports | Use `import_batch_id` and source record hash. |
| Notification retries | Use `notification_delivery_id`; retry delivery, not notification creation. |
| Export regeneration | Create versioned exports; do not overwrite released exports silently. |
| Workflow transition retries | Use `workflow_action_id`; transition may execute once only. |

## Prohibited Outcomes

Retries must not create duplicate approvals, duplicate HRMPSB recommendations, duplicate appointments, duplicate service record entries, duplicate leave ledger entries, duplicate attendance adjustments, or duplicate payroll exports marked as official.

## Recovery Rule

If idempotency cannot be proven, stop automatic retry and require manual review.
