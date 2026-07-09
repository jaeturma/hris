# Refactor Prompt

Use this prompt for controlled refactoring.

```text
Refactor the specified part of this DepEd HRIS project without changing user-visible behavior.

Target:
[FILES / MODULE / BEHAVIOR]

Reason:
[READABILITY / TESTABILITY / PERFORMANCE / AUTHORIZATION CLARITY / AUDITABILITY / DOMAIN MODELING]

Constraints:
- Read AGENTS.md and relevant .codex/*.md files.
- Do not modify Laravel core or vendor files.
- Do not change authentication flow.
- Do not install packages.
- Do not introduce unrelated HRIS modules.
- Preserve existing routes, permissions, audit behavior, database records, and Inertia page behavior unless explicitly requested.

Refactor goals:
- Improve Laravel, React, Inertia, or database structure while preserving behavior.
- Keep DepEd terminology intact.
- Preserve Region, Division, District, School, and Implementing Unit scoping.
- Preserve Data Privacy and government records safeguards.
- Keep or improve Pest coverage.

Before finishing, summarize behavior preserved, files changed, checks run, and residual risks.
```
