# Workflow Architecture

HR workflows must be stateful, auditable, permission-gated, and office-scoped.

## Workflow Pattern

Each workflow should define:

- Draft, submitted, reviewed, approved, rejected, cancelled, and finalized states where applicable.
- Submitter, reviewer, HRMPSB participant, approving authority, records officer, and auditor responsibilities.
- Required documents or evidence.
- Competency references when the process affects recruitment, placement, performance, learning, promotion, reclassification, succession, or rewards.
- Audit events and retention expectations.

## Competency-Aware Lifecycle

- Recruitment starts from a position profile and required competencies.
- Selection records applicant qualification and competency evidence.
- Placement validates position fit and office assignment.
- Performance compares actual results and behaviors against expectations.
- Competency assessment records proficiency evidence and gaps.
- Learning and development creates IDPs from gaps.
- Promotion and reclassification use readiness evidence.
- Rewards and recognition use performance and demonstrated competency evidence.

## Implementation Rule

Do not implement workflow logic until its state model, permissions, office scope, audit events, and competency touchpoints are documented.
