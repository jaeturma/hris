# Environment and Release Strategy

## Environments

| Environment | Data/access/configuration behavior |
|---|---|
| Local | synthetic data; developer access; local secrets; mail/SMS log/fake; local queue/storage; debug allowed; disposable backup |
| Shared development | synthetic only; team access; centralized non-production secrets/logs; sandbox integrations |
| Automated test | generated synthetic fixtures; isolated credentials/database; fakes; deterministic queues |
| Staging | production-like anonymized/synthetic data; restricted team access; real queue/private storage; monitored; debug off |
| UAT | approved synthetic/anonymized scenarios; named testers; sandbox delivery; acceptance evidence and backups |
| Production | real data; least privilege; managed secrets; approved providers/workers/private storage; centralized logs/monitoring; debug off; encrypted backups |
| DR | replicated/restore-ready protected data; emergency access; tested RPO/RTO and failover procedures |

Production data is never copied to development without approved anonymization. Secrets, signing credentials and certificates are never committed.

Release types are development build, internal test, UAT, pilot, production, hotfix and emergency security release. Use semantic application versions (`v0.x` internal, `v1.0.0` first production baseline); separately record schema migration set, policy configuration version, workflow version and template version. Every release has notes/changelog, included/excluded work, risk, migration/rollback and approvals.

