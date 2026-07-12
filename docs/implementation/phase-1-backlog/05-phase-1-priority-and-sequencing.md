# Priority and Sequencing

P0: WP-01-01–05/07, condition-driven remediation WP-01-06, WP-02-01 identifiers, WP-03-01 model review, office-scope design/security, bootstrap audit and any Critical/High remediation. P1: remaining required organization, authorization, audit, reference, registry and shell packages. P2: convenience UI/query/display packages that do not unlock security. P3: explicitly optional enhancements; none may introduce later-wave business scope.

Safe parallelism: documentation/token/layout prototypes after WP-1; reference classification after conventions; audit naming/config review after office context design; shell primitives without office switching. Unsafe parallelism: schema before identifiers/history; hierarchy and scope against changing models; UI switcher before server context; roles before bootstrap audit; policy activation before authority/audit; hardening before integrated features.

Release-slice order, not epic numbering alone, controls execution. A downstream package requires accepted dependencies, not merely “in progress.”

```mermaid
flowchart LR
  I[Approved identifiers/conventions] --> S[Reviewed schema package]
  S --> M[Separately approved migration]
  M --> C[Constraints/history tests]
  C --> R[Verified reference sources/stewards]
  R --> D[Production-safe seeder package]
  D --> T[Idempotency/rerun tests]
  T --> A[Data/DB/Security acceptance]
```
