# Approval Authority

Approval authority must be explicit, office-scoped, workflow-scoped, and auditable.

## Approval Concepts

- Approving authority is not the same as system administrator.
- Approval permissions must be separated by workflow type.
- Approval actions must record actor, role context, office scope, timestamp, action, remarks, and prior state.
- Users should not approve records they prepared, evaluated, or verified unless a documented exception exists.

## Approval Areas

| Workflow | Typical approving roles | Required controls | Audit sensitivity |
| --- | --- | --- | --- |
| Vacancy publication | HR Chief, RD/SDS delegate, Approving Officer | Confirm office scope, item status, publication details | high |
| Appointment recommendation | HRMPSB Chair, HR Chief, Approving Officer | Preserve ranking/evaluation basis | high |
| Appointment approval | Regional Director, Schools Division Superintendent, delegated Approving Officer | Verify recommendation and item details | high |
| Promotion cycle | HR Chief, HRMPSB Chair, Approving Officer | Preserve criteria, evidence, scores | high |
| Reclassification request | RD/SDS/delegated Approving Officer | Verify plantilla, QS, competency/performance evidence | high |
| Leave application | School Head, Approving Officer | Confirm leave balance and office scope | medium |
| Attendance adjustment | Approving Officer, School Head, HR Chief | Confirm reason and evidence | high |
| Competency profile approval | HR Chief, competency governance approver | Version profile and preserve effective dates | high |
| IDP approval | Supervisor, HR L&D role | Confirm gap basis and intervention | high |
| Document verification | Records Officer, Document Verifier | Preserve verification result and actor | high |

## Approval Permissions

Use workflow-specific permissions when practical, for example:

- `appointments.approve`
- `reclassification-requests.approve`
- `leave-applications.approve`
- `attendance-adjustments.approve`
- `position-competency-profiles.approve`

General `workflows.approve` may be used only with a Policy that verifies workflow type, assignment, and office scope.

## Notes Before Implementation

Create approval flow decision records before seeding approval steps. Verify DepEd/CSC approval routes manually per workflow.
