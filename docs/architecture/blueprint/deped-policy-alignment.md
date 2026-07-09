# DepEd Policy Alignment

DepEd hiring, placement, promotion, appointment, and reclassification issuances are the primary implementation guide for this HRIS. CSC PRIME-HRM and CBHRMS strengthen strategic HR management, but DepEd workflow rules drive operational behavior.

## Policy Guide Areas

- DepEd Order No. 007, s. 2023
- DepEd Order No. 021, s. 2024
- DepEd Order No. 020, s. 2024
- DepEd Order No. 024, s. 2025
- DepEd Order No. 034, s. 2025
- Central Office, Regional Office, and Division Office memoranda on hiring, ranking, promotion, appointment, reclassification, and personnel actions
- CSC rules and Qualification Standards
- CSC PRIME-HRM
- CSC Resolution No. 2600005 on Competency-Based HRMS
- Data Privacy Act
- Government records management requirements

## Architecture Rule

Do not hardcode scoring, ranking, qualification, document, or approval rules until the exact source issuance or memorandum has been verified and documented.

## Configurable Policy Layer

Future implementation should separate policy-configurable values from code:

- Documentary requirement sets
- Evaluation criteria
- Scoring weights
- Ranking categories
- Output templates
- Approval paths
- Publication deadlines
- Position-specific competency requirements
