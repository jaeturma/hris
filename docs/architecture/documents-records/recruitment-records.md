# Recruitment Records

## Purpose

Define records for recruitment, selection, HRMPSB, ranking, and appointment recommendation.

## Record Types

Vacancy publication, applicant profile, application documents, Qualification Standards evidence, screening results, evaluation sheets, interview records, assessment records, HRMPSB records, conflict-of-interest declarations, recusal records, deliberation minutes or metadata, ranking records, CAR/CAR-RQA/RQA-style outputs where applicable, appointment recommendation, applicant notices, appeal or protest records, and final selection records.

## Architecture Rules

- Preserve immutable snapshots of evidence and rules used during evaluation.
- HRMPSB restricted records require cycle-specific access.
- Applicant documents remain applicant-owned until converted or referenced in employee records.
- Released ranking or registry-style outputs must preserve policy, assessment framework, and template versions.
- Appeals or protests must preserve original decision snapshots.

## Source of Truth

Recruitment structured records own application, screening, evaluation, ranking, and recommendation data. Documents are evidence or generated official outputs.

## Manual Validation

CAR, CAR-RQA, RQA-style outputs, appeal/protest handling, publication records, and local memorandum requirements must be validated before implementation.
