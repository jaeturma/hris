# Phase 1 Risk and Blocker Register

| WP/epic | Risk | Sev/P/I | Owner/mitigation | Block/resolution | Slice/status |
|---|---|---|---|---|---|
| 01 | unknown baseline/tool failures | High/M/H | Lead/QA; inspect non-destructively | blocks WP-2 until C-07 disposition | 1/Open |
| 02/03 | identifier/organization ambiguity | High/H/H | Architect/DB/Org; ADR + logical scenarios | blocks migrations until C-02/03 | 1–2/Open |
| 03 | oversized model work/architecture drift | Medium/M/M | Architect; 13 independent WPs/change control | each WP independently accepted | 2/Controlled |
| 04 | cross-office leakage/stale context | Critical/M/H | Security; server scope and negative matrix | no sensitive access until review | 3/Open |
| 05 | bad defaults/admin overreach/expired authority | High/M/H | HR/Security; least privilege/SoD/validity tests | C-05 and bootstrap audit | 3/Open |
| 06 | missing actor/office/reason or audit growth | High/M/H | Governance/DPO/Records; catalog/redaction/retention | C-06 and audit tests | 3–4/Open |
| 07 | duplicate/unverified seed data | High/M/H | Data/Policy; source register/idempotency | C-04 and seeder evidence | 4/Open |
| 08 | policy activation without authority/wrong version | High/M/H | Policy/HR/Security; maker-checker/version tests | registry only; no rules engine | 5/Open |
| 09 | frontend trusted for scope/inaccessible action | High/M/H | UI/Security/QA; server props + accessibility | C-13/security acceptance | 5/Open |
| all DB | rollback/lock/history loss | High/M/H | DB Reviewer; staged migrations/rehearsal/forward repair | separate migration approval | 2–5/Open |
| all | incomplete tests/unrelated Codex changes | High/M/H | QA/Codex Operator; bounded instruction/DoD | acceptance blocked | all/Controlled |
| 10 | hidden dependency/weak acceptance | High/M/H | Project/QA; 12 separate hardening WPs | Phase 1 cannot close | 6/Open |

