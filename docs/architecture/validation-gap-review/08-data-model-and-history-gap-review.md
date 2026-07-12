# Data Model and History Gap Review

| Gap | Evidence/challenge | Severity / gate |
|---|---|---|
| Identifier/public reference decision | C-02 open | High; blocks first migration |
| Organization hierarchy cardinality/restructuring | C-03; architecture is conceptual | High; define effective parentage, moves, closure/merger and historical reporting |
| Temporal overlap/uniqueness rules | histories required but exact constraints absent | High by entity; approve before migrations |
| Appointment ownership | Wave 2 language risks duplicated history | High; correct logical ownership before workforce design |
| Snapshot schemas | policy/workflow/QS/assessment/framework snapshots required | Medium now, High before policy modules |
| Correction/supersession records | principle exists; per-entity semantics vague | High before official actions/records |
| Office ownership on shared/sensitive entities | scope principle exists | High before each sensitive schema |
| Source/provenance and import batch | migration plan exists | High before seeding/import |
| Retention/legal-hold metadata | records architecture exists; schedule unapproved | High before records module |
| Soft deletion | prohibited for completed official history in principle | Medium; table-by-table decision required |

Required negative designs: historic records missing current required fields, overlapping assignments/items, office reorganized during an active case, policy effective mid-workflow, correction after finalization, source identifier collision and archived/held record access. Current conceptual entities are too vague for migrations in Organization, authority/delegation, audit minimum, policy applicability and external reference provenance until C-02–06 close.

