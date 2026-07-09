# Data Model Overview

The data model must separate office hierarchy, reference data, position data, applicant data, employee records, workflow transactions, competency evidence, documents, and audit logs.

## Major Data Concepts

- Applicant
- Employee
- Position
- Position Title
- Plantilla Item
- Item Number
- Salary Grade
- Office / Station
- School / Implementing Unit
- Vacancy
- Publication
- Application
- Documentary Requirement
- Qualification Standard
- Evaluation Criteria
- Evaluator
- HRMPSB
- Assessment
- Interview
- Ranking
- Comparative Assessment Result
- Appointment
- Personnel Movement
- Reclassification Request
- Promotion Track
- Career Progression Level
- Competency Model
- Competency Dictionary
- Position Competency Profile
- Competency Assessment
- Individual Development Plan
- Performance Rating
- 201 File Document
- Audit Log

## Design Rules

- Keep applicant records separate from employee records until appointment or employment linkage is established.
- Keep vacancy, publication, application, evaluation, ranking, recommendation, and appointment tracking as separate but related records.
- Preserve historical qualification standards, evaluation criteria, competency requirements, and ranking basis used for a decision.
- Keep Position, Plantilla Item, Item Number, Salary Grade, and Position Competency Profile distinct.
- Link Service Record updates to the underlying Appointment or Personnel Movement.
- Link promotion, reclassification, and career progression records to position, performance, competency, and policy evidence.
- Apply office scope and document access rules to all employee, applicant, HRMPSB, and competency records.
