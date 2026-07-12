# Phase 1 Foundation Scope

## Objective

Create the smallest secure, tested foundation needed by later HRIS domains. Phase 1 approval is development approval only; migration and production approvals remain separate.

## Included

| Area | Included outcome | Acceptance boundary |
|---|---|---|
| Baseline/conventions | verified stack/scripts; naming, identifiers, dates/timezone, audit conventions | documented passing or owned corrective plan |
| Organization | office types, Region/Division/District/School/IU/office/unit/section/station structure and effective hierarchy | constraints, ancestry/scope tests, approved references |
| Office context | user-office assignments, primary/active context, server resolver | cannot select or query unauthorized scope |
| Authorization | Phase 1 roles/permissions, Laravel Policy pattern, temporary/acting authority minimum | technical admin denied HR authority; matrix tests |
| Audit | actor, subject, office context, authority/acting capacity, reason/correlation and sensitive changes | append-oriented, redacted and tested |
| References | approved minimal catalogs and production-safe seeders | idempotent, version/provenance, non-destructive |
| Policy registry | minimal policy/source metadata, versions/effective dates, verification/activation | no policy rules/scoring engine |
| Application shell | authenticated layout, domain navigation, office switcher, standard states, error/denied pages | responsive/accessibility/security evidence |
| Quality | Pest/static/format/types/lint/build baseline and CI-ready commands | all approved checks pass |

## Excluded

Full employee/workforce, plantilla, recruitment/HRMPSB, appointment/CSC processing, promotion, career progression, reclassification, personnel movements, 201 files/full document management, signatures/PNPKI, generic workflow/rules engines, policy scoring, competency/performance/L&D, leave, attendance, payroll, rewards, relations, separation, production data migration, advanced reports/analytics, AI and external integrations beyond explicit foundation interfaces.

## Foundation acceptance

Foundation acceptance requires documented scope, logical schema and migrations reviewed separately, authorization/scope/audit tests, synthetic data only, idempotent seeders, quality pipeline, updated ADR/traceability, privacy/security review and human sign-off. It does not authorize the next business module automatically.

