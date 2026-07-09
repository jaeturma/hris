# Security Architecture

Security must combine Spatie Permission RBAC, office scope, workflow state, document sensitivity, and audit trail.

## Access Layers

- Authentication through the existing project auth flow.
- Role and permission checks through Spatie Laravel Permission.
- Policy checks for model-specific access.
- Office scope filtering for Region, Division, District, School, Implementing Unit, and Office / Station.
- Workflow state checks for draft, submitted, reviewed, approved, rejected, cancelled, and finalized records.
- Document sensitivity controls for applicant files, 201 File Documents, HRMPSB records, performance ratings, and competency assessments.

## Sensitive Areas

- Applicant documents
- Evaluation and ranking records
- HRMPSB deliberation evidence
- Appointment tracking files
- Promotion and reclassification evidence
- 201 File Documents
- Performance Ratings
- Competency Assessments and IDPs
- Audit Logs

## Design Rules

- Enforce authorization server-side.
- Log sensitive exports and status changes.
- Avoid exposing full personal details in broad lists.
- Require explicit permissions for viewing evaluation details, ranking outputs, and audit logs.
- Treat AI assistance as decision support only, never final authority.
