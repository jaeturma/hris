# Fix Bug Prompt

Use this prompt when asking Codex to investigate and fix a bug.

```text
Investigate and fix this bug in the DepEd HRIS project at D:\lara\www\hris.

Bug:
[DESCRIBE BUG]

Expected behavior:
[EXPECTED]

Observed behavior:
[OBSERVED]

Known affected users or office scope:
[REGION / DIVISION / DISTRICT / SCHOOL / IMPLEMENTING UNIT / UNKNOWN]

Constraints:
- Read AGENTS.md and relevant .codex/*.md files first.
- Do not modify Laravel core or vendor files.
- Do not change authentication flow unless the bug is explicitly in auth and I approve the approach.
- Do not install packages.
- Keep the fix minimal and consistent with existing patterns.

While fixing:
- Check permissions, office scoping, validation, audit logging, database state, and Inertia props.
- Add or update Pest tests that reproduce the bug and prove the fix.
- Run the narrowest relevant tests and any formatting/static-analysis checks warranted by the change.
```
