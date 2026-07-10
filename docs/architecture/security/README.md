# Security Architecture

This folder defines the Phase 0.4 role and permission architecture for the DepEd-first, PRIME-HRM-aligned, competency-based HRIS.

This is documentation only. Do not create code, migrations, seeders, routes, controllers, models, policies, or React pages from this folder until the role matrix, office scoping rules, approval flows, and audit event names are approved.

## Architecture Rules

- Use Spatie Laravel Permission for role and permission assignment.
- Use Laravel Policies for authorization decisions.
- Do not hardcode role checks in controllers.
- Sensitive records require explicit permissions and office-scope checks.
- Employee self-service can access own records only unless additional roles are granted.
- Applicant self-service can access own applicant profile, applications, and submitted documents only.
- HRMPSB and evaluator access must be limited to assigned cycles, vacancies, applications, or assessment tasks.
- Document access must be logged.
- Administrative permission changes must be audited.

## Files

- `role-catalog.md`: role definitions, scope, major permissions, restrictions, and audit sensitivity.
- `permission-matrix.md`: permission groups and recommended permission names.
- `data-scope-rules.md`: system, regional, division, district, school/IU, own-record, applicant, HRMPSB, and evaluator scope rules.
- `approval-authority.md`: approval role architecture and approval controls.
- `document-access.md`: 201 file, applicant document, and restricted document access model.
- `audit-logging-strategy.md`: actions requiring audit logs.
- `segregation-of-duties.md`: rules to avoid conflicting privileges.
- `implementation-notes.md`: future Spatie Permission and Laravel Policy guidance.
