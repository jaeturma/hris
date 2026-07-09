# Promotion and Reclassification Data

## Purpose

Define data for promotion to higher teaching positions, expanded career progression, reclassification requests, personnel movement effects, support documents, assessments, and approvals.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `promotion_tracks` | Career or promotion track references. | `id`, `code`, `name`, `description`, `is_active` | Parent of applications and levels | yes | medium |
| `promotion_applications` | Employee applications for promotion. | `id`, `employee_id`, `promotion_track_id`, `vacancy_id`, `status`, `submitted_at` | Parents employees, tracks, optional vacancies | no | high |
| `reclassification_requests` | Position or personnel reclassification requests. | `id`, `employee_id`, `plantilla_item_id`, `requested_position_title_id`, `justification`, `status` | Parents employees/items/positions | no | high |
| `career_progression_levels` | Expanded career progression levels. | `id`, `promotion_track_id`, `code`, `name`, `sequence`, `requirements_summary` | Parent promotion tracks | yes | medium |
| `supporting_documents` | Supporting document metadata for promotion/reclassification. | `id`, `supportable_type`, `supportable_id`, `document_type_id`, `storage_reference`, `status` | Polymorphic parent; document types | no | high |
| `assessment_results` | Assessment outcomes for promotion or reclassification. | `id`, `assessable_type`, `assessable_id`, `evaluator_id`, `criteria_id`, `score`, `remarks` | Polymorphic parent; evaluators | no | high |
| `approval_histories` | Approval action history for workflows. | `id`, `approvable_type`, `approvable_id`, `step_name`, `action`, `acted_by`, `acted_at` | Polymorphic parent; users | no | high |

## Main Fields

Use employee, position, plantilla, competency profile, performance rating, status, evaluator, approver, policy reference, effective date, and source document fields.

## Relationships

Promotion applications and reclassification requests link to employee, position, plantilla, competency, performance, and assessment evidence. Approval histories track workflow actions. Approved outcomes should feed appointments, personnel movements, and service records.

## Indexing Considerations

Index employee IDs, promotion track, career level, status, submitted/effective dates, approver IDs, polymorphic supportable/approvable columns, and requested position fields.

## Data Ownership

Owned by HR career and personnel action staff, HRMPSB participants, approving authorities, and records officers.

## Data Visibility Rules

Restrict promotion/reclassification evidence, assessments, and approvals to authorized HR, HRMPSB, supervisors, approving authorities, auditors, and employee self-view where allowed.

## Audit Requirements

Audit submissions, evidence changes, assessment updates, approvals, returns, denials, reclassification decisions, and personnel movement creation.

## Seeder Requirements

Seed promotion tracks and career progression levels only after manual verification of DepEd career progression guidance.

## Notes Before Migration Creation

Decide whether promotion applications reuse recruitment application tables or remain separate. Confirm career progression and reclassification workflow states.
