# Business Process Engineering

This folder defines the Business Process Engineering (BPE) layer for the DepEd-first, PRIME-HRM-aligned, competency-based HRIS.

These documents describe how HR work should flow across DepEd Regional Offices, Schools Division Offices, Implementing Units, and Large Schools. They are not application code, migration plans, or legal opinions.

## Governing Rule

Business processes must remain stable even when a DepEd Order, memorandum, CSC rule, or local office instruction changes. Implementation must use configurable policy references, criteria, approval paths, document checklists, forms, and report templates instead of hardcoding policy details into application code.

## Distinctions

| Layer | Meaning |
| --- | --- |
| Business Process | The recurring HR work performed by people and offices. |
| Applicable Policy Area | The DepEd, CSC, privacy, records, or PRIME-HRM guidance that informs the work. |
| System Workflow | The digital steps, records, statuses, permissions, approvals, and audit logs that support the work. |
| Automation Opportunity | Deterministic assistance such as reminders, checklist validation, report generation, routing, and status tracking. |
| Future AI Opportunity | Human-reviewed assistance such as summarization, completeness checks, anomaly detection, draft recommendations, and policy-aware guidance. |

## Process Catalog

| File | Process Area |
| --- | --- |
| `01-human-resource-lifecycle.md` | Complete employee and applicant lifecycle. |
| `02-workforce-planning.md` | Staffing demand, vacancy planning, and competency planning. |
| `03-plantilla-management.md` | Plantilla item and position inventory control. |
| `04-recruitment-selection-appointment.md` | General recruitment, selection, and appointment. |
| `05-teacher-hiring.md` | Teacher hiring and registry-style outputs. |
| `06-school-administrator-promotion.md` | School head and administrator promotion. |
| `07-non-teaching-hiring.md` | Non-teaching recruitment and appointment. |
| `08-career-progression.md` | Expanded career progression. |
| `09-reclassification.md` | Reclassification requests and review. |
| `10-employee-onboarding.md` | Appointment-to-employee onboarding. |
| `11-personnel-movement.md` | Transfers, reassignment, detail, and other movements. |
| `12-service-record-management.md` | Service record creation, correction, and issuance. |
| `13-201-files-management.md` | Personnel document lifecycle. |
| `14-leave-management.md` | Leave application, approval, and ledger. |
| `15-attendance-timekeeping.md` | Attendance, DTR, and correction flows. |
| `16-learning-development.md` | L&D planning and intervention tracking. |
| `17-competency-management.md` | Competency model, assessment, and gap management. |
| `18-performance-management.md` | Performance planning, rating, and linkage. |
| `19-rewards-recognition.md` | PRAISE-aligned rewards and recognition. |
| `20-discipline-grievance.md` | Discipline and grievance documentation support. |
| `21-separation-retirement.md` | Separation, retirement, clearance, and records closure. |
| `22-records-retention.md` | Retention, access, disposition, and archival control. |
| `23-document-approval-routing.md` | Reusable document routing and approval process. |
| `24-prime-hrm-alignment.md` | PRIME-HRM readiness and evidence management. |
| `25-ai-automation-opportunities.md` | AI and automation governance pipeline. |

## Rating Definitions

| Rating | Automation Meaning | AI Readiness Meaning |
| --- | --- | --- |
| Low | Process needs heavy human judgment or policy clarification. | Not enough clean data or high risk if AI assists. |
| Medium | Some steps can be standardized, routed, or validated. | AI can assist with summaries or checks after data improves. |
| High | Rules, documents, statuses, and outputs are predictable. | AI can assist with reviewed recommendations or exception detection. |
| Very High | High-volume, repeatable, auditable process with clear inputs and outputs. | Strong candidate for human-reviewed AI assistance after governance approval. |

## Implementation Rule

Future modules must begin from these process documents, then map to data tables, permissions, UI screens, workflow states, audit events, and tests. Do not build a feature directly from a policy title alone.
