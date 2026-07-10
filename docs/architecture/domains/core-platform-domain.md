# Core Platform Domain

## Purpose

Support the whole HRIS with user access, authentication-adjacent records, authorization, notifications, settings, audit logs, feature flags, and file storage references.

## Business Scope

Users, authentication integration, roles, permissions, sessions, notifications, system settings, audit logs, feature flags, and file storage references.

## Out of Scope

HR policy interpretation, employee identity, office hierarchy, personnel actions, and document verification.

## Main Entities

User, Role, Permission, Session, Notification, System Setting, Audit Log, Feature Flag, File Storage Reference.

## Aggregate or Ownership Candidates

User account, role assignment, permission assignment, notification, audit log entry, feature flag.

## Key Business Rules

- Use Spatie Laravel Permission for RBAC.
- Core Platform supports HR domains but does not own HR policy.
- Administrative access changes must be audited.
- File storage references do not replace Personnel Records document ownership.

## Commands or Use Cases

Create user, assign role, grant permission, revoke permission, create notification, record audit event, enable feature flag.

## Domain Events

UserCreated, RoleAssigned, PermissionChanged, NotificationSent, AuditEventRecorded, FeatureFlagChanged.

## Dependencies

Depends on Organization for office context. Provides identity and audit support to all domains.

## Policy Dependencies

Data Privacy Act, government audit requirements, system security policies, DepEd access governance.

## Security Sensitivity

Restricted.

## Audit Requirements

Log login-relevant security events, role changes, permission changes, system setting changes, audit exports, and file reference changes.

## Reports Produced

User access report, role assignment report, permission audit, activity log report, feature flag status report.

## Implementation Phase

Phase 1 foundation.
