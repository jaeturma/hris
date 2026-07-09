# Permission Strategy

Authorization must be explicit, scalable, auditable, and compatible with Spatie Laravel Permission.

## Philosophy

- Use roles to group responsibilities.
- Use permissions to authorize actions.
- Use policies for model-aware decisions.
- Use gates for cross-cutting or non-model actions.
- Enforce every sensitive action on the server.
- Use React only to improve UX by hiding unavailable controls.

## Role Families

Future role design may include:

- Regional HR Administrator
- Division HR Administrator
- School HR Staff
- Implementing Unit HR Staff
- HRMPSB Member
- Approving Authority
- Records Officer
- Read-only Auditor
- System Administrator

Do not create these roles until the module and governance rules are approved.

## Permission Names

Use `resource.action` naming:

- `employees.view`
- `employees.create`
- `plantilla-items.update`
- `appointments.approve`
- `service-records.export`
- `audit-logs.view`

Separate view, create, update, approve, reject, cancel, export, import, restore, and audit permissions.

## Office Scope

Permissions alone are not enough. Every sensitive query must also respect office scope:

- Region users may need cross-division visibility.
- Division users may need division and school visibility.
- School or implementing-unit users must be limited to assigned offices.
- Auditors may be read-only but broad in scope.

## Approval Workflows

Approval workflows must define:

- Submitter
- Reviewer
- HRMPSB participant, when relevant
- Approving authority
- Return or rejection path
- Finalization rules
- Audit events

Avoid hardcoding approval assumptions before policy and office practice are documented.
