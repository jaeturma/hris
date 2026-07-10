# Queue and Job Strategy

## Purpose

Define which operations may use queues and which must remain synchronous.

## Recommended Queued Operations

Email sending, SMS sending, report generation, large exports, document processing, virus scanning, OCR, search indexing, analytics refresh, integration synchronization, batch reminders, and escalation checks.

## Recommended Synchronous Operations

Authorization checks, validation, workflow state transition, approval recording, rejection recording, data integrity checks, critical audit record creation, and policy version locking.

## Queue Priorities

| Priority | Examples |
| --- | --- |
| Critical | Audit-adjacent integration acknowledgments, security alerts. |
| High | Time-sensitive reminders, escalation alerts, digital signature status checks. |
| Normal | Email/SMS delivery, report jobs, export jobs. |
| Low | Analytics refresh, search indexing, digest notifications. |

## Retry and Timeout Strategy

Use bounded retries. Jobs that call external services need timeouts, backoff, idempotency keys, and failed-job records. Do not retry a job that may create duplicate approvals or duplicate personnel actions.

## Sensitive Payload Rule

Queued payloads must use record references and minimal metadata. Do not place full documents, full personal data, scores with sensitive comments, or restricted case contents in queued payloads.

## Failed Job Handling

Failed jobs require monitoring, manual replay where safe, failure reason, idempotency key, related workflow, and responsible support role.
