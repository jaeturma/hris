# Phase 0.10 Policy Engine, AI, Analytics, and Decision-Support Architecture

This folder defines the policy engine, rules architecture, AI governance, analytics, and decision-support architecture for HRIS for DepEd.

This is documentation only. Do not create production migrations, models, controllers, React pages, routes, jobs, services, or executable business logic from this folder.

## Purpose

The architecture enables HRIS for DepEd to register policies, version rules, determine policy applicability, configure qualification and assessment frameworks, support analytics, provide advisory decision support, govern AI, preserve human accountability, and reproduce recommendations.

## Core Principles

- Policy-driven, not controller-driven.
- Policies are authoritative references after verification and approval.
- Official transactions preserve exact policy, rule, workflow, document, competency, and template versions.
- Human authority remains required for appointment, promotion, reclassification, rejection, ranking finalization, signatures, records disposition, and discipline.
- Deterministic rules perform official eligibility and scoring computations.
- AI is advisory, source-bound, reviewable, auditable, and never an unauthorized decision-maker.
- Analytics are read-oriented and must not modify operational records.
- Recommendations must be explainable and reproducible.

## Required Documents

| File | Purpose |
| --- | --- |
| `01-policy-engine-overview.md` | Policy engine boundaries and lifecycle. |
| `02-policy-registry-and-versioning.md` | Registry, statuses, versions, and lifecycle diagram. |
| `03-policy-applicability-and-resolution.md` | Applicability, hierarchy, conflict, and resolution flow. |
| `04-rules-engine-architecture.md` | Configurable deterministic rules engine. |
| `05-qualification-standard-engine.md` | QS architecture and validation snapshots. |
| `06-assessment-configuration-engine.md` | Assessment frameworks and official ranking controls. |
| `07-workflow-policy-mapping.md` | Policy-to-workflow configuration snapshots. |
| `08-policy-exceptions-and-overrides.md` | Exception and override controls. |
| `09-ai-governance-framework.md` | AI governance, risk, approval, and monitoring. |
| `10-ai-use-cases-and-prohibited-actions.md` | Permitted and prohibited AI actions. |
| `11-ai-document-and-record-assistance.md` | OCR, document AI, and human verification. |
| `12-competency-and-career-decision-support.md` | Competency, IDP, readiness, and career assistance. |
| `13-workforce-analytics-architecture.md` | Workforce analytics and data flow. |
| `14-prime-hrm-and-compliance-analytics.md` | PRIME-HRM/compliance analytics. |
| `15-executive-dashboard-architecture.md` | Dashboard audiences and controls. |
| `16-decision-support-architecture.md` | Decision-support service and review states. |
| `17-explainability-and-human-validation.md` | Explainability and reviewer controls. |
| `18-ai-security-privacy-and-risk-controls.md` | AI privacy/security boundary. |
| `19-knowledge-base-and-policy-retrieval.md` | Approved knowledge base and source validation. |
| `20-data-model-and-entity-catalog.md` | Conceptual entity catalog. |
| `21-events-workflows-and-integration.md` | Events and integrations aligned with Phase 0.8. |
| `22-audit-retention-and-reproducibility.md` | Audit, retention, reproducibility. |
| `23-testing-and-validation-strategy.md` | Pest-oriented validation strategy. |
| `24-phased-implementation-roadmap.md` | Implementation roadmap and gates. |
| `25-phase-completion-review.md` | Completion checklist, gaps, and Phase 0.11 items. |

## Security Rule

Use Laravel Policies, Spatie Permission, office-level data scope, assigned-workflow scope, HRMPSB-cycle scope, evaluator-assignment scope, employee/applicant ownership scope, restricted-record access, segregation of duties, temporary delegated authority, and least privilege. Do not rely on React role checks as the primary security control.

## Policy and AI Permissions

| Permission | Purpose |
| --- | --- |
| Register policy | Create policy registry entries. |
| Verify policy | Confirm source and metadata. |
| Approve policy | Approve policy for activation/configuration. |
| Activate policy | Make approved policy version available for new transactions. |
| Supersede policy | Replace active policy version. |
| Configure rules | Create structured rules from approved policy. |
| Publish rules | Activate rule set version. |
| Request exception | Ask for policy exception or equivalency. |
| Approve exception | Approve policy exception with business authority. |
| Configure assessment | Create framework version. |
| Activate assessment framework | Make framework available to cycles. |
| Request AI assistance | Generate advisory AI result. |
| Review AI recommendation | Accept, partially accept, reject, or invalidate advisory result. |
| View restricted analytics | View sensitive dashboards. |
| Export analytics | Export reports and dashboard data. |
| Manage AI models | Register model/provider/configuration. |
| Approve AI deployment | Authorize AI use case/model deployment. |
| Review AI incidents | Handle AI/security incidents. |
| Access policy-conflict cases | View and resolve conflict cases. |

## Non-Functional Expectations

| Area | Expectation |
| --- | --- |
| Availability | Policy and workflow resolution should be available during HR processing windows. |
| Scalability | Support large applicant, document, and analytics volumes. |
| Performance | Cache approved policy/rule definitions safely while preserving version correctness. |
| Security | Enforce server-side authorization and least privilege. |
| Privacy | Minimize personal data in AI, analytics, queues, and exports. |
| Accessibility | Dashboards and decision-support UI must remain accessible. |
| Maintainability | Policy content is configured and versioned, not buried in code. |
| Testability | Rules and frameworks must have deterministic test cases. |
| Explainability | Advisory and deterministic outputs must show basis and limitations. |
| Traceability | Outputs link to policies, rules, evidence, workflow, user, and office. |
| Reproducibility | Preserve inputs, versions, model/prompt details, and outputs. |
| Resilience | Handle AI provider outages, policy conflicts, incomplete data, and queue failures. |
| Data quality | Flag missing/inconsistent data instead of guessing. |
| Observability | Monitor rule failures, AI incidents, analytics refresh, and data quality. |
| Interoperability | Integrate through adapters and versioned payloads. |
| Auditability | High-impact actions and recommendations require immutable audit records. |

## Prohibited Architecture Shortcuts

Do not hardcode DepEd point systems in controllers; use generative AI for official scoring; treat uploaded policy PDFs as automatically active; use one generic promotion workflow; allow administrators to bypass HR authority; replace HRMPSB deliberation with algorithmic ranking; store only the latest policy version; apply new policies retroactively without transition rules; overwrite completed evaluation results; treat scanned signatures as certificate-based digital signatures; send sensitive records to public AI services; allow analytics queries to alter operational records; hide AI limitations; generate recommendations without source or explanation; automatically delete government records; mix policy documents, structured rules, and workflow definitions into one uncontrolled record; or use role checks in React components as sole security control.
