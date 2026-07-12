# AI, Analytics, and Decision-Support Gap Review

AI remains correctly deferred and cannot reject/disqualify/rank officially, alter scores, approve appointments/promotions/reclassification, sign, dispose records, replace HRMPSB or replace appointing authority.

| Area | Missing control/evidence | Status |
|---|---|---|
| governance/model/provider | approval criteria, inventory, vendor risk, model/version retirement | Red for production |
| prompt/retrieval security | injection defenses, office/document ACL enforcement, restricted-source filtering | Red |
| citations/explainability/review | source-version citations, limitations, reviewer/disposition record | Architecture principle only |
| privacy/bias/accuracy | DPIA, representative synthetic evaluation, thresholds and incident rollback | Red |
| availability/incident | provider outage fallback, kill switch, breach/model incident runbooks | Red |
| metrics/lineage | owner/definition/source/as-of/freshness/snapshot/restricted dimensions | Amber design, Red for advanced analytics |
| advisory/official distinction | labeling and write prohibition documented | Green principle; verify in UI/API tests later |

No AI work package may be inferred from Wave 10 until a separate controlled pilot architecture and approvals exist. Analytics may read scoped operational snapshots but may not write business truth.

