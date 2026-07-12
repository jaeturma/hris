# Risk, Assumption, Issue, and Dependency Register

Target dates are expressed as due conditions because no approved calendar or named assignees were supplied. Role owners must be replaced with named accountable people at mobilization.

| ID | Type | Description | P/I/Severity | Owner | Mitigation / contingency | Due condition | Status | Blocks |
|---|---|---|---|---|---|---|---|---|
| R-01 | Risk | Policy changes/misinterpretation or conflicting local issuance | H/H/High | Policy Validator | verified registry, applicability/conflict review; pause affected module | before affected backlog ready | Open | affected module |
| R-02 | Risk | Broken office scope exposes cross-office data | M/H/Critical | Security Reviewer | server scope contract + matrix tests; disable affected release | before first sensitive entity | Open | Phase 1 schema/business data |
| R-03 | Risk | Poor/incomplete historical and reference data | H/H/High | Data Owner | profile, provenance, trial reconciliation; manual exception queue | before import/reference activation | Open | affected data |
| R-04 | Risk | Generic workflow/rules engines create coupling | M/H/High | Architect | concrete-first ADR and design review; remove from scope | every work package | Controlled | affected design |
| R-05 | Risk | Unauthorized document access/storage growth | M/H/High | Security/Records | private storage, classification, access log, capacity/retention; suspend upload | before document stage | Open | documents |
| R-06 | Risk | Audit omissions or unbounded growth | M/H/High | Governance/Infra | minimum event catalog, redaction, indexes, retention/archive monitoring | before audit migration/production | Open | audit production |
| R-07 | Risk | Premature AI use/bias/privacy breach | M/H/Critical | System Owner/DPO | enforce ADR-005/010 and Phase 1 exclusion; shut off provider | before any AI PoC | Controlled | AI |
| R-08 | Risk | External API/PNPKI delays | H/M/High | Integration Owner | adapters, sandbox, manual fallback; defer integration | before integration backlog | Open | integration only |
| R-09 | Risk | Large applicant/query volumes degrade service | M/M/Medium | Architect/DB Reviewer | volume targets, indexes, pagination/load test; capacity scaling | before recruitment acceptance | Open | recruitment release |
| R-10 | Risk | Insufficient validation/training/change management | M/H/High | Project/HR Owner | named reviewers, UAT/training plan; delay rollout | before UAT/pilot | Open | release |
| R-11 | Risk | Deployment resources/restore capability inadequate | M/H/High | Deployment Admin | RPO/RTO, monitored backups, restore exercise; no production | before production | Open | production |
| A-01 | Assumption | Authoritative office hierarchy and plantilla sources can be obtained | —/H/High | Data Owner | confirm steward/source; limit seed to verified subset | before relevant schema/seed | Unvalidated | relevant work |
| A-02 | Assumption | HR owners/policy validators will review workflows promptly | —/H/High | Project Owner | assign alternates/SLAs; re-sequence work | before module mobilization | Unvalidated | affected module |
| A-03 | Assumption | Policies may be stored/processed lawfully | —/M/Medium | Legal/DPO | rights/privacy review; store metadata/link only | before policy-source files | Unvalidated | source storage |
| A-04 | Assumption | Existing Laravel starter/auth baseline is stable | —/M/Medium | Lead Developer | WP-1 inspection; corrective baseline task | WP-1 | Unvalidated | WP-2 onward |
| I-01 | Issue | Identifier/public-reference strategy not approved | —/H/High | Architect/DB Reviewer | decision record and examples | before first migration | Open | first migration |
| I-02 | Issue | Organization logical model/cardinalities not signed off | —/H/High | Organization Owner/Architect | schema review with hierarchy cases | before org migration | Open | org migration |
| I-03 | Issue | Phase 1 permission/scope/audit minimum catalogs not frozen | —/H/High | Security/HR/Architect | executable matrix and event fields | before security migrations | Open | foundation security |
| I-04 | Issue | Quality commands have not been executed as readiness evidence | —/M/Medium | QA/Lead Developer | WP-1 non-destructive baseline | WP-1 completion | Open | WP-2 |
| I-05 | Issue | Retention schedules, infrastructure and signature trust unapproved | —/H/High | Records/Infra/Legal | formal reviews; keep excluded | before affected stage | Open | documents/production |
| D-01 | Dependency | Management approves scope, roles, risks and Phase 1 entry | —/H/High | Project Owner | recorded approval | before Phase 1 | Pending | Phase 1 |
| D-02 | Dependency | Security/privacy review of office scope and classifications | —/H/High | Security/DPO | review evidence and residual risk decision | before sensitive data | Pending | business data |
| D-03 | Dependency | Budget/procurement/infrastructure/external services | —/M/Medium | System Owner | staged plan and fallbacks | before affected environment | Pending | production/integrations |

