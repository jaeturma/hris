# 09 AI Governance Framework

## Purpose

Define AI governance suitable for a Philippine government HR system.

## AI Risk Classification

| Risk | Examples | Required Controls |
| --- | --- | --- |
| Low | Text summarization, drafting internal summaries, formatting assistance. | User review, source display, audit for sensitive records. |
| Medium | Document completeness hints, competency gap summaries, dashboard narratives. | Approved sources, human validation, access scope, logging. |
| High | Promotion-readiness indicators, succession-readiness indicators, policy applicability assistance. | Formal use-case approval, explainability, reviewer decision, monitoring. |
| Prohibited | Final ranking, appointment, disqualification, promotion approval, discipline finding. | Blocked by design. |

## AI Lifecycle

Identify use case, classify risk, perform privacy/security review, approve source data, define prompt/model version, pilot with controlled users, validate outputs, monitor issues, approve deployment, review periodically, suspend when unsafe.

## AI Governance Roles

AI use-case owner, HR process owner, data protection reviewer, security reviewer, policy reviewer, technical owner, human reviewer, auditor.

## Governance Rule

AI output is advisory and must be distinguishable from official decisions. Acceptance, partial acceptance, rejection, or correction must be recorded for high-impact recommendations.
