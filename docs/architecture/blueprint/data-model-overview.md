# Data Model Overview

The data model must separate reference data, official HR records, transactional workflow records, competency evidence, and audit history.

## Reference Data

- Regions, Divisions, Districts, Schools, Implementing Units
- Position Titles
- Salary Grades
- Job Families
- Competency Models
- Competency Dictionary
- Proficiency Levels
- Behavioral Indicators

## Position and Competency Data

- Plantilla Items
- Item Numbers
- Position Profiles
- Position-to-Competency Mapping
- Required proficiency levels
- Effective dates for position requirements

## Employee and HR Records

- Employee profile
- Government employment details
- 201 file metadata
- Service records
- Leave records
- Appointment, promotion, transfer, reclassification, and separation records

## Competency Transaction Data

- Competency assessments
- Competency evidence
- Competency gap analysis
- Individual Development Plans
- Learning and Development interventions
- Succession planning readiness
- Promotion readiness
- Rewards and recognition linkage

## Design Rules

- Preserve the competency requirements used for a decision at the time of decision.
- Avoid hard deletes for official HR and competency evidence records.
- Use audit logs for changes to competency dictionaries, mappings, assessments, and readiness indicators.
- Apply office scope and privacy rules to all employee-linked competency data.
