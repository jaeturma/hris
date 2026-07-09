# Audit and Security Data

## Purpose

Define security, RBAC, approval, access logging, and audit tables that protect sensitive DepEd HR data.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `users` | Authenticated system users. | `id`, `name`, `email`, `employee_id`, `is_active`, timestamps | Parent of actions and roles | no | high |
| `roles` | Spatie role table. | `id`, `name`, `guard_name` | Spatie permissions | yes | high |
| `permissions` | Spatie permission table. | `id`, `name`, `guard_name` | Spatie roles | yes | high |
| `model_has_roles` | Spatie model-role pivot. | `role_id`, `model_type`, `model_id` | Users/roles | yes/config | high |
| `model_has_permissions` | Spatie direct permission pivot. | `permission_id`, `model_type`, `model_id` | Users/permissions | no | high |
| `activity_log` | Spatie Activitylog event records. | `id`, `log_name`, `description`, `subject_type`, `subject_id`, `causer_type`, `causer_id`, `properties`, `event` | All auditable records | no | high |
| `approval_flows` | Configurable approval workflow definitions. | `id`, `code`, `name`, `applies_to`, `is_active` | Parent approval steps | yes/config | high |
| `approval_steps` | Steps in approval flows. | `id`, `approval_flow_id`, `step_order`, `role_id`, `action_required` | Parent flows/roles | yes/config | high |
| `approval_actions` | Actual approval actions. | `id`, `approval_flow_id`, `approvable_type`, `approvable_id`, `step_id`, `action`, `acted_by`, `acted_at` | Workflow records/users | no | high |
| `data_access_logs` | Sensitive view/export/access log. | `id`, `user_id`, `record_type`, `record_id`, `access_type`, `purpose`, `accessed_at` | Users and sensitive records | no | high |

## Main Fields

Use actor, subject, office scope, event/action, status, purpose, IP/user-agent where appropriate, and properties that avoid excessive personal data.

## Relationships

Users may link to employees. Spatie tables govern RBAC. Activity logs and data access logs reference sensitive records. Approval flows define reusable workflow steps; approval actions record actual decisions.

## Indexing Considerations

Index user IDs, role/permission names, subject type/ID, causer type/ID, event, access timestamp, approvable type/ID, and approval status/action fields.

## Data Ownership

Owned by system administrators, security administrators, and authorized auditors.

## Data Visibility Rules

Security and audit data are high-sensitivity. Restrict to administrators, auditors, and authorized oversight users.

## Audit Requirements

Audit role/permission changes, approval configuration changes, sensitive data access, export, and administrative actions.

## Seeder Requirements

Seed roles, permissions, and approval flow templates only after RBAC and workflow decision records are approved.

## Notes Before Migration Creation

Use package migrations for Spatie tables. Define whether office-scoped roles need custom assignment tables before implementation.
