# Policy and Requirements Traceability

## Traceability flow

```mermaid
flowchart LR
  P[Policy / requirement] --> BP[Business process] --> D[Domain] --> E[Entity]
  E --> R[Rule] --> W[Workflow] --> PM[Permission]
  PM --> DOC[Document] --> EV[Event] --> A[Audit] --> T[Test]
```

## Policy traceability register

No provision below is treated as verified merely from its title. The DepEd policy validator must capture the official source, relevant provision, effective/supersession dates and applicability before rule implementation.

| ID | Authority / issuance | Process / domain | Intended artifacts | Security/audit/test | Phase | Status |
|---|---|---|---|---|---|---|
| POL-001 | DepEd Order 007 s. 2023 | Recruitment and Selection | policy version, criteria/checklist/workflow snapshots | assigned evaluators; score/decision audit; policy scenarios | Recruitment | Requires validation |
| POL-002 | DepEd Order 020 s. 2024 | Career/HR process (applicability to confirm) | versioned rules and required records | authority/scope tests | Affected module | Requires validation |
| POL-003 | DepEd Order 021 s. 2024 | Affected HR process to be confirmed | policy record and trace links | validator approval | Affected module | Unverified |
| POL-004 | DepEd Order 024 s. 2025 | Career progression / personnel action | pathway, evidence and decision snapshots | separation from vacancy promotion; history tests | Later wave | Requires validation |
| POL-005 | DepEd Order 034 s. 2025 | Affected HR process to be confirmed | versioned configuration | policy and authority tests | Later wave | Unverified |
| POL-006 | CSC MC 08 s. 2025 | Appointment/personnel action | applicability and action records | appointing authority and audit tests | Appointment | Requires validation |
| POL-007 | CSC 2025 ORAOHRA | Appointment and CSC action | appointment/QS/action snapshots | immutable decisions; effective-date tests | Appointment | Requires legal/policy review |
| POL-008 | CSC PRIME-HRM | Governance/competency/analytics | maturity evidence and advisory metrics | lineage and access tests | Cross-cutting | Framework validation required |
| POL-009 | CSC Resolution 2600005 | CBHRMS | competency framework/version | HR owner approval and version tests | Competency | Requires validation |
| POL-010 | Approved Merit Selection Plan | Recruitment/promotion | MSP version, assessment, deliberation | HRMPSB assignment/recusal/score audit | Per office/cycle | Source not supplied |
| POL-011 | Regional/Division Memoranda | Local applicability | scoped policy version/precedence | office applicability and conflict audit | Per module | Source not supplied |
| POL-012 | Data Privacy Act and issuances | All sensitive domains | classification, purpose, retention/access rules | privacy review, access/export tests | Foundation onward | Legal mapping required |
| POL-013 | Government records rules | Records/documents | retention, hold, disposition, transfer | records approval and immutable audit | Records | Schedule not approved |

## Requirements register

| ID | Type | Requirement / source | Priority | Owner | Phase | Acceptance / test | Status |
|---|---|---|---|---|---|---|---|
| FR-001 | Functional | Model Region, Division, District, School, IU, office/unit/station; architecture | Must | Organization | 1 | hierarchy and effective-date scenarios | Traced |
| SEC-001 | Security | Server-enforced office isolation; security architecture | Must | Core/Organization | 1 | same/cross/oversight scope matrix | Traced; design approval pending |
| SEC-002 | Authorization | Technical admin has no implied HR authority; ADR-011 | Must | Governance | 1 | policy denial tests | Traced |
| DAT-001 | Data | Preserve personnel and assignment history; data rules | Must | Owning domains | 1+ | no destructive overwrite tests | Traced |
| AUD-001 | Audit | Attribute sensitive actions with actor, office, authority, reason and correlation | Must | Governance | 1 | activity assertions/redaction | Traced; minimum fields pending |
| PRI-001 | Privacy | Minimize, restrict and log sensitive access/exports | Must | Governance | 1+ | serialization/export/access tests | Traced |
| REC-001 | Records | Preserve originals, versions, holds and disposition authority | Must | Personnel Records | Records wave | lifecycle tests | Blocked by schedule review |
| ACC-001 | Accessibility | Keyboard, focus, semantics, errors and contrast | Must | UI | 1 | manual + automated checks | Protocol pending |
| QUA-001 | Quality | Pest, static analysis, formatting, types and production build pass | Must | Quality | 1 | CI-equivalent commands | Verify baseline in WP-1 |
| INT-001 | Integration | Adapter, authentication, idempotency, retry and audit per integration | Should | Integration | Later | contract/failure tests | Deferred by design |
| REP-001 | Reporting | Scoped, reproducible reports with freshness and export audit | Must | Analytics | Later | lineage/scope/snapshot tests | Deferred by design |
| AI-001 | AI governance | Advisory, approved sources, explainable, reviewable, auditable | Must | Policy/Analytics | Later | prohibited-action and review tests | Not implementation-ready |
| PERF-001 | Performance | Define volume/service targets before affected module | Should | Architecture | Before module | load budget and query tests | Missing targets |
| AVL-001 | Availability | Backup, restore, monitoring and DR objectives approved | Must before production | Infrastructure | Pre-production | restore exercise/evidence | Not evidenced |
| DQ-001 | Data quality | Provenance, validation, reconciliation and exceptions for imports | Must | Data Migration | Before import | trial reconciliation | Framework traced |

## Required implementation trace record

Every work package shall list policy IDs, requirement IDs, architecture and ADR references, owner, entities, office scope, permissions, workflow, documents, events, audit, tests, acceptance evidence, limitations and validation status.

