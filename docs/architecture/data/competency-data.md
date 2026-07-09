# Competency Data

## Purpose

Define CBHRMS and PRIME-HRM aligned data for competency models, dictionaries, proficiency levels, behavioral indicators, position profiles, assessments, gap analysis, and IDPs.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `competency_models` | Competency framework versions. | `id`, `code`, `name`, `description`, `effective_from`, `effective_to`, `status` | Parent of competencies | yes | medium |
| `competencies` | Competency dictionary entries. | `id`, `competency_model_id`, `competency_category_id`, `code`, `name`, `description`, `is_active` | Parents `competency_models`, `competency_categories` | yes | medium |
| `competency_categories` | Core, leadership, functional/technical categories. | `id`, `code`, `name`, `description`, `sort_order` | Parent of `competencies` | yes | low |
| `competency_levels` | Proficiency levels. | `id`, `code`, `name`, `level_number`, `description` | Used by indicators and mappings | yes | medium |
| `behavioral_indicators` | Observable indicators by competency and level. | `id`, `competency_id`, `competency_level_id`, `indicator_text`, `is_active` | Parents `competencies`, `competency_levels` | yes | medium |
| `position_competency_profiles` | Competency requirements for position profiles. | `id`, `position_title_id`, `job_family_id`, `salary_grade_id`, `effective_from`, `status` | Parents position and competency references | yes/config | high |
| `employee_competency_assessments` | Employee assessment results. | `id`, `employee_id`, `position_competency_profile_id`, `assessment_period`, `assessor_id`, `status` | Parents `employees`, profiles, users | no | high |
| `competency_gap_analyses` | Computed or validated competency gaps. | `id`, `employee_id`, `assessment_id`, `competency_id`, `required_level_id`, `assessed_level_id`, `gap_value` | Parents assessments and competencies | no | high |
| `individual_development_plans` | IDPs tied to gaps and L&D actions. | `id`, `employee_id`, `assessment_id`, `status`, `approved_by`, `period_start`, `period_end` | Parents employees and assessments | no | high |

## Main Fields

Include model/version codes, effective dates, status, assessor/approver IDs, assessment periods, required and assessed proficiency levels, evidence references, and office scope.

## Relationships

Competency models own competencies; competencies own behavioral indicators by level. Position profiles map positions to required competencies. Employee assessments compare employees against profile requirements. Gap analyses feed IDPs.

## Indexing Considerations

Index competency codes, model/category IDs, position profile IDs, employee IDs, assessment period, assessor ID, status, and effective dates.

## Data Ownership

Competency administrators own dictionary and mapping data. HR, supervisors, or authorized assessors own assessments and IDPs.

## Data Visibility Rules

Competency dictionary can be broadly visible. Assessments, gaps, IDPs, readiness, and evidence are sensitive and office/role-scoped.

## Audit Requirements

Audit all changes to competency definitions, levels, indicators, mappings, assessments, gaps, and IDP approvals.

## Seeder Requirements

Seed only verified competency models, categories, levels, and indicators. Treat draft competency libraries as configurable reference data.

## Notes Before Migration Creation

Decide how to version competency profiles so past recruitment, promotion, and performance decisions preserve the exact requirements used.
