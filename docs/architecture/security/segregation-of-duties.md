# Segregation of Duties

Segregation of duties prevents one user from controlling a sensitive workflow from start to finish.

## Core Rules

- A user who prepares a record should not be the sole approver.
- A user who evaluates an applicant should not unilaterally approve the appointment.
- A user who verifies a document should not silently replace it later without audit.
- A Security Administrator should not be an HR workflow approver by default.
- A System Administrator should not use technical access for normal HR decisions.
- A Records Officer should not modify evaluation scores.
- A Payroll/Fiscal role should not access HRMPSB deliberation records by default.

## Conflict Examples

| Conflict | Risk | Rule |
| --- | --- | --- |
| HR Officer + Approving Officer on same transaction | Self-approval | Policy must block self-approval unless documented exception |
| Evaluator + Ranking approver | Score manipulation | Require separate HRMPSB/approver review |
| Security Administrator + HR Chief | Privilege escalation | Require dual approval for role grants |
| Document Verifier + Restricted Document Manager | Document tampering | Log replacements and require records review |
| Payroll Exporter + Attendance Adjuster | Payroll manipulation | Separate adjustment approval from export |

## Implementation Notes

Future Policies must receive the record and current workflow state, then verify whether the current user has a conflict with prior actions on that record.

Use approval history and activity logs to check:

- creator/preparer,
- verifier,
- evaluator,
- recommender,
- approver,
- releaser.
