# Implementation Notes

These notes guide future implementation. Do not create seeders or code until the matrix is approved.

## Spatie Permission

- Use Spatie Laravel Permission for roles and permissions.
- Keep role names human-readable.
- Keep permission names machine-readable using `resource.action`.
- Prefer permissions over role checks in application logic.
- Avoid direct permissions except for exceptional user-specific grants.
- Cache permission lookups using package conventions.

## Laravel Policies

Use Policies when authorization depends on:

- office scope,
- record ownership,
- workflow assignment,
- applicant/employee self-service,
- HRMPSB cycle membership,
- evaluator assignment,
- workflow state,
- document sensitivity,
- segregation of duties.

Controllers should call Policy-backed authorization, not `hasRole()` branches.

## Avoiding Privilege Escalation

- Only Security Administrator or Super Administrator can manage roles/permissions.
- Role grants must be audited.
- Assigning high-risk roles should require approval or review.
- Do not grant `Super Administrator` for normal HR operations.
- Separate security administration from HR approval duties.
- Review direct user permissions regularly.

## Seeder Strategy

Seed first:

- System roles.
- Core security permissions.
- Read-only auditor role.
- Basic organization and employee view permissions.
- Document access and audit log permissions.

Defer workflow-heavy permissions until workflow states and policy rules are approved.

## Testing Expectations

Future implementation must include Pest authorization tests for:

- each role category,
- each data scope,
- own-record access,
- applicant self-service,
- HRMPSB limited-cycle access,
- evaluator limited-assignment access,
- restricted document access,
- self-approval prevention,
- export logging.
