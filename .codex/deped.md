# DepEd Domain Rules

This HRIS must reflect Philippine public education HR operations. Codex must not design generic corporate HR workflows when DepEd concepts apply.

## Core Organizational Concepts

- Region: DepEd regional office with oversight across divisions.
- Division: Schools Division Office responsible for schools and division personnel actions.
- District: grouping used for school administration and reporting.
- School: school-level unit where teaching and non-teaching personnel may be assigned.
- Implementing Unit: school or office with delegated administrative or fiscal functions.

Every feature that stores or displays HR data must define the office scope it belongs to.

## Core Personnel Concepts

- Employee: person employed, appointed, assigned, separated, or otherwise tracked by the HRIS.
- Plantilla Item: authorized position slot.
- Item Number: government position item identifier.
- Position Title: official title tied to qualification and compensation rules.
- Salary Grade: compensation level used for government positions.
- Qualification Standards: required education, experience, training, and eligibility.

Do not treat position title, salary grade, item number, and plantilla item as interchangeable.

## Personnel Actions

Personnel actions must be history-preserving and auditable. This includes Appointment, Promotion, Reclassification, Transfer, Separation, Hiring, Placement, Leave transactions, Performance Rating updates, and Service Record changes.

Use effective dates, approving authority, office scope, supporting references, and audit metadata where applicable.

## HRMPSB and Merit Selection

Recruitment, hiring, placement, and promotion features must be policy-aware. They should support vacancy and plantilla item details, qualification standards, applicants and eligibility, screening and ranking, HRMPSB actions, appointing authority decisions, posting, notice, and records requirements.

Do not implement scoring or ranking rules without explicit, current policy confirmation.

## Policy Areas

Use these as policy context, not as copied legal text: CSC PRIME-HRM; CSC Resolution No. 2600005; Agency Competency-Based Human Resource Management System; DepEd hiring, placement, promotion, and reclassification guidelines; DepEd Order No. 007, s. 2023; DepEd Order No. 020, s. 2024; DepEd Order No. 024, s. 2025; Civil Service Commission rules; Data Privacy Act; and government records management requirements.

When exact eligibility, ranking, documentary, or retention rules matter, verify them from official sources before implementation.

## PRIME-HRM and CBHRMS Foundation

This HRIS must align with meritocracy and excellence in government HRM. Competency-Based Human Resource Management System principles are a core architecture foundation, not a future add-on.

Every major HR lifecycle process must be able to reference competencies:

- Recruitment compares applicant qualifications and competencies against position profiles.
- Selection and placement consider position competency requirements.
- Performance management connects ratings with competency expectations.
- Learning and development addresses competency gaps through Individual Development Plans.
- Promotion and reclassification use competency evidence, readiness, and merit selection alignment.
- Succession planning tracks readiness for leadership and critical roles.
- Rewards and recognition link to performance and demonstrated competencies.

Codex must model competency-aware concepts such as Competency Model, Core Competencies, Leadership Competencies, Functional or Technical Competencies, Competency Dictionary, Job Family, Position Profile, Position-to-Competency Mapping, Proficiency Levels, Behavioral Indicators, Competency Gap Analysis, Individual Development Plan, Learning and Development Intervention, Succession Planning Readiness, Promotion Readiness, Performance Rating Linkage, Rewards and Recognition Linkage, Merit Selection Plan Alignment, SPMS Alignment, and PRAISE Alignment.

## Records and Privacy

- 201 files are sensitive personnel records.
- Service records must be accurate, traceable, and protected from silent edits.
- Performance ratings and recruitment documents require strict role-based access.
- Data minimization applies: collect only the fields needed for the HR process.
- Exports must be controlled, justified, and audit-logged.

## Language and Labels

Use government HR terminology in labels and documentation. Prefer terms like `Plantilla Item`, `Item Number`, `Salary Grade`, `Appointment`, `Service Record`, `HRMPSB`, and `201 Files` over generic equivalents.
