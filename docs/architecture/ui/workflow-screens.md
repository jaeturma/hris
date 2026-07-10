# Workflow Screens

Workflow screens must show status, evidence, assigned actors, next action, and audit history.

## Shared Pattern

Each workflow screen should include:

- Page header with status badge.
- Office scope and policy/reference context.
- Summary panel.
- Evidence/document checklist.
- Timeline or stepper.
- Main work area.
- Approval/action panel.
- Audit history drawer.

## Workflow UI Patterns

| Workflow | UI pattern | Key screen elements |
| --- | --- | --- |
| Recruitment cycle | Pipeline dashboard plus vacancy detail | Publication status, applications count, screening queue, HRMPSB cycle, ranking output |
| Applicant screening | Checklist review screen | Application summary, documents, QS checklist, screen/return/disqualify actions |
| Evaluation | Assigned scoring workspace | Criteria, evidence, score inputs, remarks, save/submit |
| HRMPSB review | Cycle workspace | Members, assigned applications, evaluation completion, deliberation notes, recommendation |
| Ranking | Controlled ranking report screen | Criteria version, computed totals, manual review notes, approval/export |
| Appointment recommendation | Recommendation packet | Applicant, vacancy, ranking basis, HRMPSB action, recommendation action |
| Promotion evaluation | Employee promotion workspace | Performance, competency evidence, documents, evaluation, readiness |
| Reclassification request | Request tracker | Current/target position, justification, supporting documents, approvals |
| Competency assessment | Assessment grid | Position profile, competencies, levels, behavioral indicators, evidence, gaps |
| Leave approval | Approval queue | Leave balance, dates, attachment, supervisor remarks, approve/return/reject |
| Attendance correction | Correction review | Original log, requested change, reason, evidence, approval |
| Document verification | Document review | Preview, metadata, checklist, verify/reject/return, access log |

## Approval Timeline UI

Timeline entries should show:

- Step name.
- Actor.
- Action.
- Timestamp.
- Remarks summary.
- Current owner.

Do not expose confidential deliberation notes to users without permission.

## Audit History UI

Use a drawer or tab with event filters. Show safe changed-field summaries. Do not display raw sensitive payloads.
