# Implementation RAID Register

Due dates are conditions until a calendar and named people are approved.

| ID | Type | Description | P/I/Severity | Owner | Mitigation / contingency | Target/due condition | Status | Block |
|---|---|---|---|---|---|---|---|---|
| R-101 | Risk | Foundation scope expansion | M/H/High | Project Owner | freeze exclusions/change control; defer extras | Phase 1/every WP | Open | affected WP |
| R-102 | Risk | Architecture drift/cross-domain coupling | M/H/High | Architect | boundary review/ADR; stop and redesign | every PR | Controlled | affected work |
| R-103 | Risk | Broken office scope/unauthorized access | M/H/Critical | Security | server scope + negative matrix; disable release | before sensitive data | Open | sensitive modules |
| R-104 | Risk | Policy validation incomplete | H/H/High | Policy Validator | source/provision/applicability gate; pause rule | before affected module | Open | affected module |
| R-105 | Risk | Incorrect reference seed data | M/H/High | Data Owner | authoritative provenance/idempotency tests; rollback/supersede | before seed approval | Open | seeding |
| R-106 | Risk | Premature generic workflow/rules engine | M/H/High | Architect | concrete-first ADR; remove scope | design review | Controlled | design |
| R-107 | Risk | Oversized Codex tasks/unrelated changes | M/M/Medium | Codex Operator | one WP, file boundary, stop conditions | task approval | Controlled | task |
| R-108 | Risk | Insufficient tests/audit/history | M/H/High | QA/Governance | DoD/quality gate; reject work | acceptance | Open | acceptance |
| R-109 | Risk | Migration rollback/lock/data loss | M/H/High | DB Reviewer | staged changes, backup, rehearsal/forward repair | migration approval | Open | migration |
| R-110 | Risk | UI inconsistency/accessibility failure | M/M/Medium | UI/QA | shared components/protocol; remediation | shell/module acceptance | Open | affected UI |
| R-111 | Risk | Performance/volume issues | M/M/Medium | Architect/DB | budgets/index/query/load tests; capacity plan | before high-volume module | Open | affected release |
| R-112 | Risk | Deployment misconfiguration/failed restore | M/H/High | Deployment Admin | config baseline/secret control/restore test | before production | Open | production |
| A-101 | Assumption | Phase 0.11 conditions can be resolved with named reviewers | —/H/High | Project Owner | mobilization assignments; hold if unavailable | before relevant gate | Unvalidated | Phase 1 |
| A-102 | Assumption | HR/policy owners and authoritative organization data are available | —/H/High | HR/Data Owners | source/availability confirmation | before design/seed | Unvalidated | relevant WP |
| A-103 | Assumption | Laravel baseline/libraries remain compatible | —/M/Medium | Lead Developer | WP-1 verification; corrective plan | WP-1 | Unvalidated | WP-2 |
| A-104 | Assumption | Staging/UAT will be available | —/H/High | System Owner | infrastructure plan; postpone release | before UAT | Unvalidated | UAT |
| I-101 | Issue | C-02 identifier strategy failed | —/H/High | Architect/DB | approve ADR/examples | before migration | Open | migration |
| I-102 | Issue | C-03 organization/scope model failed | —/H/High | Org/Architect/Security | approve logical model/scenarios | before org migration | Open | WP-3/4 |
| I-103 | Issue | C-04 source/steward catalog failed | —/H/High | Data/Policy | approve source register | before seed | Open | WP-7 |
| I-104 | Issue | C-05/06 authority/audit not frozen | —/H/High | Security/HR/Governance | executable matrices/catalog | before protected mutation | Open | WP-4–8 |
| I-105 | Issue | C-07 baseline not verified | —/M/Medium | Lead/QA | execute WP-1 | before WP-2 | Open | WP-2 |
| I-106 | Issue | C-01/08/14/15 approval/clean baseline pending | —/H/High | Project/Lead | record approvals/owners/isolate work | before WP-1 | Open | WP-1 |
| D-101 | Dependency | Management, security, privacy, records and policy approvals | —/H/High | Project Owner | scheduled gates/alternates | relevant phase | Pending | relevant work |
| D-102 | Dependency | Infrastructure, external APIs, time and testing resources | —/H/High | System Owner | capacity/procurement/fallback plan | before affected work | Pending | release/integration |
