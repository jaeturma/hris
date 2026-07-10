# 29 Assessment Framework Engine

## Purpose

Define how assessment frameworks are versioned, linked to policies, applied to cycles, and snapshotted for completed evaluations without hardcoding scoring criteria or point allocations.

## Trigger

New hiring cycle, promotion cycle, career progression pathway, reclassification evaluation, teacher hiring cycle, local memorandum, or assessment framework update.

## Actors

HR policy owner, assessment administrator, evaluator, HRMPSB secretariat, competency administrator, auditor.

## Inputs

Policy version, effectivity period, assessment framework version, criteria groups, document requirements, rating scales, competency references, evaluator assignments, report templates, transition notes.

## High-Level Process Flow

1. Register assessment framework version and policy basis.
2. Define criteria categories, evidence sources, evaluator roles, and outputs as configuration.
3. Link framework to pathway, position group, QS version, competency framework, and MSP version.
4. Lock framework when a cycle opens.
5. Apply framework to applications or employee records.
6. Preserve immutable snapshots of criteria, evidence, ratings, scores, evaluator actions, and outputs.

## Decision Points

- Which policy version and effectivity period authorizes the framework?
- Does the framework apply to teacher hiring, non-teaching hiring, higher teaching promotion, Master Teacher progression, School Principal progression, or reclassification?
- Are criteria and point allocations verified by HR/legal before configuration?
- What happens to pending cycles when a framework changes?

## Outputs

Assessment framework register, locked cycle framework, evaluation snapshots, criteria version report, transition flags.

## Applicable Policy Area

DepEd Orders and Memoranda on hiring, promotion, appointment, reclassification, and career progression; CSC appointment and HR action rules; PRIME-HRM; CBHRMS.

## PRIME-HRM Contribution

Supports transparent, merit-based, auditable Recruitment/Selection/Placement and competency-based HR decisions.

## Competency-Based HRM Link

Assessment frameworks may include competency evidence, behavioral indicators, proficiency levels, gap analysis, promotion readiness, and succession readiness.

## System Responsibilities

Keep frameworks configurable and versioned. Lock applied versions per cycle. Preserve immutable evaluation snapshots. Prevent retroactive edits to completed evaluations.

## Automation Opportunity Rating

Very High - framework locking, scoring calculation, validation, routing, and reports are automatable after verified configuration.

## AI Readiness Rating

Medium - AI can summarize evidence and explain missing items but must not generate official scores or rankings without reviewed deterministic rules.

## AI Opportunities

Evidence summaries, missing requirement detection, evaluator packet preparation, transition warnings, and anomaly detection.

## Reports Produced

Assessment framework register, cycle criteria report, evaluation snapshot report, scoring audit report, transition impact report.

## Security Considerations

Restrict framework approval, evaluator records, applicant evidence, scores, comments, and generated rankings.

## Future Integrations

Document Management, Digital Signature, AI Assistant, Government Portals.

## Related Business Processes

Policy Versioning, Merit Selection Plan, HRMPSB Governance, Recruitment Selection Appointment, Career Progression.
