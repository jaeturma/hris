# Domain and Module Gap Review

| Boundary | Validation | Gap / remediation |
|---|---|---|
| Organization → Workforce | single office/hierarchy owner | define restructuring snapshots and assignment references |
| Workforce ↔ Appointment | potential ownership ambiguity in Wave 2 wording | Appointment owns appointment truth; Workforce exposes employment/personnel view and consumes completed-action handoff |
| Workforce ↔ Plantilla | person versus authorized item separated | distinguish position assignment from plantilla item occupancy and temporal conflicts |
| Plantilla → Recruitment | vacancy derived/authorized, not freely created | formal vacancy authorization contract and snapshot |
| Recruitment → Appointment | selected-candidate handoff separated | define immutable handoff payload/revocation/correction; no cross-table writes |
| Career ↔ Plantilla/Appointment | career case distinct from resulting item/personnel action | define approved-outcome handoffs per pathway |
| Personnel Records ↔ all domains | documents support structured truth | each domain owns record; Records owns file metadata/version/access, not decision |
| Policy ↔ operational domains | policy configuration separate | operational transaction owns snapshot; Policy domain cannot rewrite cases |
| Workflow ↔ domain status | workflow coordinates, domain owns truth | concrete state mapping and failure behavior required |
| Reporting/Analytics | read-oriented | prohibit operational write-back; define lineage/snapshot contracts |
| Integration | adapter boundary | inbound commands must re-enter application authorization/validation |

No missing/god domain or unavoidable cycle was found. The appointment-history ambiguity is High because wrong ownership could force redesign. Most handoff-contract gaps are Medium and must close before the relevant module becomes Architecture Ready.

