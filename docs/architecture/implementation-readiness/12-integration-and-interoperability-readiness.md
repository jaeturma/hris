# Integration and Interoperability Readiness

## Integration register

| Integration | Direction/data | Classification/auth | Reliability/audit | Earliest phase / status |
|---|---|---|---|---|
| Email | outbound notifications | contact + case metadata; provider credential | queued, retry/idempotency, delivery logs | foundation notification later; interface unconfirmed |
| SMS/mobile push | outbound alerts | phone/device token; provider auth | consent, throttling, delivery reconciliation | later; deferred |
| Biometrics | inbound attendance | sensitive identifiers/time logs; device/API auth | staged import, dedupe, exception reconciliation | attendance; API unconfirmed |
| Payroll systems | bidirectional/export preparation | restricted employment/financial data | batch IDs, encryption, reconciliation, approval | payroll prep; interface unconfirmed |
| DepEd/CSC systems | exchange/reference/status | sensitive official records; mutually approved auth | contracts, idempotency, audit and failure queue | affected later phase; no stable API assumed |
| PNPKI | signature request/validation | certificates/signing credentials | timestamp, revocation and immutable evidence | signature stage; blocked by trust design |
| Identity provider | authentication/identity claims | identity data; OIDC/SAML if approved | claim mapping, deprovisioning, security logs | future; baseline remains existing auth |
| Private storage | file read/write | highly sensitive; service credentials | checksums, access logs, backup/restore | records foundation; platform unconfirmed |
| Reporting/L&D/SIS | scoped exchange | varies; least privilege | adapter contract and reconciliation | later; interface unconfirmed |
| Approved AI service | request/response | potentially sensitive; explicit approval | minimization, provenance, audit, incident handling | AI phase; prohibited now |

Each integration must use a domain-neutral interface and vendor adapter, typed contract, secret configuration, timeout/retry policy, idempotency key, failure/dead-letter handling, correlation/audit, test double, sandbox mode, classification/privacy assessment and availability fallback. Domain code cannot call vendor APIs directly or accept external writes without authorization and validation.

**Assessment: Gray for Phase 1, otherwise Red/Amber by integration.** No external API availability is assumed.

