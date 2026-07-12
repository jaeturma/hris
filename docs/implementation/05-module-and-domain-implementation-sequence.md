# Module and Domain Implementation Sequence

## State model

Proposed → Architecture ready → Backlog ready → Development ready → In development → Under review → Testing → Accepted → Released. Deferred and Blocked are explicit side states; neither counts as complete.

## Dependency matrix

| Code / module / owner | Predecessors and references | Policy/permission/scope | Workflow/doc/event/test | Wave / block |
|---|---|---|---|---|
| ORG Organization | baseline, identifiers, office references | offices.manage; hierarchy scope | effective change; `OfficeHierarchyChanged`; constraint/scope tests | 1 / C-02–04 |
| SCP Office Scope | ORG, user-office assignments | context permission + Policy/ancestry | assignment history; `OfficeContextChanged`; cross-office matrix | 1 / C-03,05 |
| IAM Roles/Authority | SCP, permission catalog | roles/permissions + delegated authority | approval assignment evidence; authority events/tests | 1 / C-05 |
| AUD Audit | SCP/IAM, audit catalog | audit access/redaction | immutable activity; correlation; audit tests | 1 / C-06 |
| REF References | identifiers, verified sources | steward permissions | provenance/version events; seeder tests | 1 / C-04 |
| POL Policy Registry | REF/IAM/AUD | policy manage/verify/activate | version/source link; `PolicyVersionActivated`; snapshot tests | 1 / C-05,06 |
| UI Shell | auth/SCP/IAM | server-provided abilities only | no business workflow; accessibility/browser tests | 1 / C-13 |
| WFM Workforce | complete Wave 1 | employee permissions/privacy/office scope | document links; history events; Policy/serialization/history tests | 2 / later approval |
| PLT Plantilla | WFM/REF | plantilla permissions/office scope | assignment/vacancy events; uniqueness/history tests | 3 / source validation |
| REC Recruitment | PLT/POL/workflow/doc controls | validated MSP, HRMPSB/evaluator assignments | application/evidence/comparative records; decision events; deterministic/scope tests | 4 / policy gate |
| APT Appointment/Actions | REC handoff/WFM/PLT | CSC/ORAOHRA and appointing authority | appointment/signature/CSC records; immutable action tests | 5 / policy/records gate |
| CPR Career/Reclassification | WFM/PLT/competency/POL | pathway-specific policies/authority | evidence and distinct workflows/events/tests | 6 / policy gate |
| CBL Competency/Performance/L&D | WFM/PLT/POL | CBHRMS/SPMS permissions | framework snapshots/evidence/events/tests | 7 / framework validation |
| PAD Personnel Admin | WFM/records/integrations | privacy/leave/attendance/records rules | files/ledgers/requests; restricted/history/reconciliation tests | 8 / records/infra gate |
| ERS Rewards/Relations/Separation | WFM/POL/records | PRAISE/legal/restricted authority | awards/cases/clearance/turnover; SoD/privacy tests | 9 / policy/legal gate |
| ANA Analytics/Integration/AI | mature accepted sources | scoped reads, approved provider/metrics | read models/adapters/recommendation review; lineage/failure/bias tests | 10 / excluded until mature |

Notifications never replace records; reporting never writes operational truth; documents support but do not own structured decisions.
