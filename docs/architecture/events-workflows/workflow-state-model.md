# Workflow State Model

## Purpose

Define a standard vocabulary for workflow states while allowing each domain to use only the states it needs.

## Standard States

Draft, Open, Submitted, Received, Under Review, Awaiting Documents, For Evaluation, For Interview, For Deliberation, For Recommendation, For Approval, Approved, Partially Approved, Returned, Rejected, Cancelled, Expired, Superseded, Finalized, Released, Archived.

## Common Transitions

| From | To | Guard | Actor | Remarks / Evidence |
| --- | --- | --- | --- | --- |
| Draft | Submitted | Required fields complete. | Owner or HR staff. | Optional unless policy requires. |
| Open | Submitted | Submission window active. | Applicant, employee, HR staff. | Required declarations. |
| Submitted | Received | Intake accepted. | HR staff or secretariat. | Receipt metadata. |
| Received | Under Review | Assigned reviewer exists. | HR staff. | Assignment record. |
| Under Review | Awaiting Documents | Deficiency found. | Reviewer. | Required deficiency remarks. |
| Awaiting Documents | Submitted | Missing evidence supplied. | Applicant, employee, HR staff. | Evidence reference. |
| Under Review | For Evaluation | Completeness and QS checks passed. | HR/evaluator. | Screening snapshot. |
| For Evaluation | For Interview | Interview required. | Evaluator/HR. | Schedule reference. |
| For Evaluation | For Deliberation | Assessment finalized. | Evaluator/secretariat. | Evaluation snapshot. |
| For Deliberation | For Recommendation | Quorum and deliberation recorded. | HRMPSB. | Deliberation metadata. |
| For Recommendation | For Approval | Recommendation completed. | HRMPSB/HR. | Recommendation record. |
| For Approval | Approved | Authority valid. | Approver. | Required decision remarks where applicable. |
| Any active state | Returned | Policy permits return. | Assigned reviewer/approver. | Required deficiency remarks. |
| Any active state | Rejected | Policy permits rejection. | Authorized actor. | Required reason. |
| Any active state | Cancelled | Cancellation permitted. | Owner/authorized HR. | Required reason. |
| Approved | Finalized | Downstream checks complete. | Owning domain. | Final snapshot. |
| Finalized | Released | Output released. | Authorized records/HR. | Release metadata. |
| Released | Archived | Retention rule applies. | Records officer/system. | Retention reference. |

## Immutable States

Finalized, Released, Archived, CSC Action Recorded, Evaluation Finalized, HRMPSB Deliberation Completed, and Appointment Issued are immutable for business history. Corrections must create new correction records or versions.

## Reopening Rules

Reopening requires policy permission, authorized actor, reason, link to original workflow, and snapshot preservation. Reopening must not erase prior decisions.

## Correction Rules

Corrections must record original value, new value, actor, office context, reason, policy version, workflow definition version, and related evidence.

## State Rule

Do not force every workflow to use every state. Use domain language and only the states needed for clear HR operations.
