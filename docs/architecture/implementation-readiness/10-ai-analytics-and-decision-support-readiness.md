# AI, Analytics, and Decision-Support Readiness

## Classification

| Capability | Classification | Reason / gate |
|---|---|---|
| AI governance and use-case design | Ready for design only | ADRs establish advisory boundaries |
| policy retrieval proof of concept | Not ready | approved corpus, access filtering, vendor/privacy/security assessment absent |
| document extraction pilot | Not ready | document foundation, representative synthetic test set and human verification absent |
| recommendations/decision support | Not ready | reliable data, policy snapshots, bias/accuracy/explainability validation absent |
| official ranking/appointment/action by AI | Prohibited | human statutory/business authority cannot be delegated to AI |
| operational foundation dashboards | Design only | transactional data and approved metric definitions absent |
| management/PRIME-HRM analytics | Deferred | lineage, freshness, data ownership and maturity evidence required |

Analytics may read approved scoped data and snapshots but cannot update operational records. Every metric needs definition, owner, source lineage, as-of/freshness indicator, office scope, privacy classification and official/advisory label. Historical reporting must preserve the applicable date/version context.

Any future recommendation must be advisory, explainable, reviewable, rejectable, versioned and auditable. Record inputs/source versions, output, confidence/limitations, reviewer and disposition. Sensitive data may not be sent to an unapproved provider.

**Assessment: Gray for Phase 1 and Red for production use.** AI and advanced analytics are expressly excluded.
