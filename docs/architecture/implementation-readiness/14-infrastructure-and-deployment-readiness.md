# Infrastructure and Deployment Readiness

## Environment readiness

| Capability | Local/test | Staging/production requirement | Status |
|---|---|---|---|
| PHP/MySQL/Node/Laravel | verify in WP-1 | supported pinned versions | Amber |
| HTTPS | `https://hris.app` local convention | valid TLS, secure cookies, proxy settings | Local expected; production unverified |
| Database | non-production synthetic data | encryption/access/backup/monitoring | Unverified |
| Queue/scheduler/Redis | sync/test may be used | supervised workers, scheduler, retry/dead-letter monitoring | Unverified |
| Private storage | local private disk for development | redundant private storage, scan, backup/restore | Unverified |
| Logs/audit/error tracking | local logs | centralized restricted logs, alerting, retention/redaction | Unverified |
| Mail/SMS | log/fake/sandbox | approved provider and safe failure behavior | Deferred |
| Backup/restore/DR | documented local recovery | RPO/RTO, encrypted backups, tested restore, DR owner | Red before production |
| Malware scanning | test double/integration point | approved scanner and quarantine | Red before file upload production |

Secrets never committed include `.env`, application/database/mail/SMS/storage/AI credentials, tokens, signing keys and PNPKI certificates. Production debug is off. Access is least-privilege and environment-separated. Production data cannot be copied to development without approved anonymization.

Required deployment evidence: environment inventory, ownership, configuration baseline, secret rotation, migration/release/rollback procedure, health monitoring, worker/scheduler supervision, log/audit capacity, backup success and restore exercise, incident contacts, file limits and DR objectives.

**Assessment: Red for production deployment; Amber for local Phase 1 baseline.** This does not block WP-1 but blocks production authorization.

