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

Use these as policy context, not as copied legal text: DepEd hiring, placement, and promotion guidelines; DepEd Order No. 007, s. 2023; DepEd Order No. 020, s. 2024; DepEd Order No. 024, s. 2025; Civil Service Commission rules; Data Privacy Act; and government records management requirements.

When exact eligibility, ranking, documentary, or retention rules matter, verify them from official sources before implementation.

## Records and Privacy

- 201 files are sensitive personnel records.
- Service records must be accurate, traceable, and protected from silent edits.
- Performance ratings and recruitment documents require strict role-based access.
- Data minimization applies: collect only the fields needed for the HR process.
- Exports must be controlled, justified, and audit-logged.

## Language and Labels

Use government HR terminology in labels and documentation. Prefer terms like `Plantilla Item`, `Item Number`, `Salary Grade`, `Appointment`, `Service Record`, `HRMPSB`, and `201 Files` over generic equivalents.
