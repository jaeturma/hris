# Integration Delivery Strategy

Each integration uses a domain-facing interface, vendor adapter, environment configuration, least-privilege authentication, typed contract, timeout/retry policy, idempotency key, reconciliation/failure queue, structured/redacted logging, business audit, test double and sandbox mode. Data classification, privacy/security review, availability fallback and ownership are approved before activation. Domain code never directly calls a vendor API or trusts inbound data to bypass authorization.

| Integration | Delivery condition |
|---|---|
| Email/SMS/mobile | consent/content minimization, queued delivery, throttling and failure independence |
| PNPKI | approved certificate/signature/timestamp/revocation trust model |
| Biometrics | device identity, staged import, deduplication and attendance reconciliation |
| Payroll/DepEd/CSC systems | official contract, batch/correlation IDs, encryption, authorization and reconciliation |
| Cloud/private storage | approved residency/access/backup/restore and access audit |
| Identity providers | approved claim mapping, provisioning/deprovisioning and security monitoring |
| Analytics/L&D systems | scoped minimal exchange, lineage and freshness |
| AI provider | approved source/data/provider/privacy/security/bias/accuracy controls; advisory only |

External APIs are never assumed available or stable; unavailable integrations remain Deferred with manual or safe failure behavior.

