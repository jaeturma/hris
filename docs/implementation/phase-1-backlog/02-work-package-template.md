# Work-Package Template

Every package uses this complete structure.

```text
Work Package ID / Epic / Task Title / Status / Priority / Wave
Owning Domain / Primary Reviewer / Risk / Complexity

1. Objective — measurable outcome.
2. Context — DepEd capability, ADR and downstream consumers.
3. Scope — exact schema/backend/frontend/tests/docs included.
4. Out of Scope — related work explicitly excluded.
5. Dependencies — exact WP IDs, data, references, permissions, decisions and human gates.
6. Architecture References — exact files/sections.
7. Policy References — verified sources or “No direct policy rule...” statement.
8. Database Changes — proposed tables/columns/types/nullability/FKs/unique/index/effective/status/version/audit/IDs/rollback; or none.
9. Backend Requirements — simplest justified Laravel patterns, validation, transaction and error behavior.
10. Frontend Requirements — Inertia/React/types/states/accessibility; or none.
11. Permissions and Authorization — names, actors, Policy methods, authority and admin limitations.
12. Office and Data Scope — ownership/ancestry/oversight and negative cases.
13. Audit Requirements — actor/role/capacity/office/entity/old-new/reason/basis/correlation.
14. Domain Events — producer/payload/consumer/sensitivity/idempotency/queue/audit; or none.
15. Validation Rules — required/format/unique/parent/effective/status/conflict/archive.
16. Security Requirements — auth/scope/CSRF/rate/serialization/mass assignment/export/files/secrets and negative cases.
17. Tests — unit/feature/Policy/scope/database/seeder/frontend/accessibility/regression/security/manual evidence as applicable.
18. Documentation Updates.
19. Acceptance Criteria — observable Given/When/Then including negative cases.
20. Definition of Done.
21. Risks and Mitigations.
22. Completion Evidence.
23. Ready-to-Paste Codex Instruction.
```

No package may invent policy or use UI hiding as authorization. A database plan is not migration approval.

