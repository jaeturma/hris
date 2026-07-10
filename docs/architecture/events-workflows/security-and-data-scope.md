# Security and Data Scope

## Purpose

Define authorization and scope checks required for workflow actions, notifications, events, and queues.

## Scope Types

Policy authorization, office data scope, assigned-workflow scope, self-service scope, applicant ownership scope, HRMPSB cycle scope, evaluator assignment scope, restricted-record scope, read-only auditor scope, digital signature authority, delegated authority, temporary assignment expiration.

## Required Checks for Every Workflow Action

1. User permission.
2. Office scope.
3. Workflow assignment.
4. Current workflow state.
5. Policy validity.
6. Required evidence.
7. Segregation-of-duties rules.

## Notification Scope

Notifications must be created only for authorized recipients. Action URLs must re-check permissions on click. SMS and email must avoid sensitive details.

## Queue Scope

Queued jobs must rehydrate current authorization-sensitive records carefully. Jobs may process system side effects but must not perform hidden human approvals.

## Restricted Workflows

Performance ratings, HRMPSB deliberations, appointment packets, CSC action, employee relations, 201 files, medical/sensitive leave documents, and payroll preparation need stricter permissions and access logging.
