# Recruitment, Selection, and Appointment Data

## Purpose

Define data for DepEd-first vacancy publication, applicant registration, applications, documents, QS checking, evaluation, HRMPSB, ranking, CAR/CAR-RQA/RQA-style outputs, appointment recommendation, and appointment tracking.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `vacancies` | Open position opportunities. | `id`, `plantilla_item_id`, `position_title_id`, `station_id`, `status`, `open_date`, `close_date` | Parents plantilla and office tables | no | high |
| `publications` | Publication notices for vacancies. | `id`, `vacancy_id`, `publication_date`, `posting_channel`, `approved_by`, `status` | Parent `vacancies` | no | medium |
| `applicants` | Applicant identity records. | `id`, `uuid`, `last_name`, `first_name`, `email`, `phone`, `privacy_consent_at` | Parent of applications | no | high |
| `applications` | Applicant application to a vacancy. | `id`, `applicant_id`, `vacancy_id`, `submission_date`, `status`, `employee_id` | Parents applicants, vacancies, optional employees | no | high |
| `documentary_requirements` | Requirement checklist per vacancy or policy set. | `id`, `vacancy_id`, `document_type_id`, `is_required`, `sort_order` | Parents vacancies, document types | yes/config | medium |
| `submitted_documents` | Applicant submitted document metadata. | `id`, `application_id`, `document_type_id`, `storage_reference`, `status`, `verified_by` | Parents applications and document types | no | high |
| `qualification_standards` | QS requirements per position/vacancy. | `id`, `position_title_id`, `education`, `experience`, `training`, `eligibility`, `effective_from` | Parents position titles | yes/config | high |
| `evaluation_criteria` | Evaluation criteria and weights. | `id`, `vacancy_id`, `criteria_name`, `weight`, `policy_reference_id`, `is_active` | Parents vacancies, policy refs | yes/config | high |
| `evaluation_results` | Evaluator results per application. | `id`, `application_id`, `evaluator_id`, `criteria_id`, `score`, `remarks`, `status` | Parents applications, users, criteria | no | high |
| `interview_results` | Interview records. | `id`, `application_id`, `evaluator_id`, `interview_date`, `score`, `remarks` | Parents applications, users | no | high |
| `rankings` | Ranking batch/list. | `id`, `vacancy_id`, `ranking_type`, `generated_at`, `approved_by`, `status` | Parent vacancies | no | high |
| `comparative_assessment_results` | CAR or related result rows. | `id`, `ranking_id`, `application_id`, `rank`, `total_score`, `remarks` | Parents rankings, applications | no | high |
| `appointment_recommendations` | Recommended applicant records. | `id`, `application_id`, `vacancy_id`, `recommended_by`, `recommended_at`, `status` | Parents applications, vacancies | no | high |
| `appointments` | Appointment tracking and official appointment metadata. | `id`, `employee_id`, `applicant_id`, `plantilla_item_id`, `appointment_status_id`, `effective_date`, `approved_by` | Parents employees/applicants/items/statuses | no | high |

## Main Fields

Use vacancy status, publication dates, applicant privacy consent, application status, evaluator IDs, policy references, criteria version, scores, recommendation and appointment status, and document metadata.

## Relationships

Vacancies connect to plantilla items and publications. Applicants submit applications. Applications own submitted documents, evaluation results, interview results, and ranking rows. Recommendations feed appointments and employee records.

## Indexing Considerations

Index vacancy status/dates, applicant UUID/email, application vacancy/applicant/status, document verification status, evaluator IDs, ranking vacancy/type, and appointment effective/status fields.

## Data Ownership

Owned by HR recruitment staff, HRMPSB secretariat, authorized evaluators, and appointing authority.

## Data Visibility Rules

Applicant documents, evaluation results, interviews, rankings, and recommendations are high-sensitivity. Restrict to assigned HR staff, evaluators, HRMPSB, approving authorities, auditors, and applicant self-view where applicable.

## Audit Requirements

Audit submission, document verification, QS results, evaluation changes, ranking generation, CAR exports, recommendations, and appointment status changes.

## Seeder Requirements

Seed document requirement templates, policy references, and evaluation criteria only after manual DepEd/CSC verification.

## Notes Before Migration Creation

Confirm exact CAR/CAR-RQA/RQA applicability, scoring, documentary requirements, HRMPSB steps, and appointment status terms before schema finalization.
