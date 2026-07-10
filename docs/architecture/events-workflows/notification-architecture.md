# Notification Architecture

## Purpose

Define multi-channel notifications for workflow actions, reminders, results, policy updates, security alerts, and escalations.

## Channels

In-app notifications, Email, SMS, future mobile push, dashboard alerts, digest notifications, and escalation alerts.

## Notification Types

Informational, action required, reminder, deadline warning, escalation, approval result, document deficiency, policy update, security alert, and system maintenance.

## Required Fields

Recipient, recipient role or assignment, office scope, related record, related workflow, notification template, channel, priority, delivery status, read status, action URL, expiration, sensitive-data classification, retry status.

## Rules

- Do not include highly sensitive personnel information in SMS.
- Email content should be minimal when sensitive records are involved.
- Notification links must still enforce authorization.
- Applicants see only their own application information.
- Employees see only their own employee-service information unless authorized.
- HRMPSB members receive notifications only for assigned selection cycles.
- Auditors do not receive operational approval assignments.
- Delivery history must be auditable.
- Failed external delivery must not change workflow status.

## Source of Truth

Workflow records, approval records, domain records, and audit history are the source of truth. Notifications are communication side effects.
