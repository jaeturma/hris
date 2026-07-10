# Audit and Immutability

## Purpose

Define structured history and immutable evidence for legally and operationally significant HR workflow decisions.

## Required Audit Records

Workflow creation, assignment, reassignment, review, approval, rejection, return, cancellation, escalation, deadline override, document verification, score finalization, HRMPSB deliberation, appointment recommendation, CSC action, notification delivery, failed delivery, digital signature request, and access to restricted records.

## Required Audit Fields

Actor, delegated or acting capacity, office context, timestamp, original value, new value, reason or remarks, policy version, workflow definition version, IP/device metadata where appropriate, and related documents.

## Dedicated History Records

Do not rely solely on generic activity logs for significant workflow decisions. Use dedicated structured history for:

- Evaluation finalization.
- HRMPSB quorum, recusal, deliberation, and recommendation.
- Appointment recommendation and appointment issuance.
- CSC submission and action.
- Leave ledger adjustments.
- Attendance corrections.
- Performance rating validation and correction.
- Competency assessment finalization.
- Restricted document access.

## Immutability Rule

Completed decisions are not edited in place. Corrections create new records or versions that reference the original decision.

## Snapshot Rule

Major workflows must preserve policy version, workflow definition version, assessment framework version, qualification-standard version, competency-framework version, actors, evidence, and state at finalization.
