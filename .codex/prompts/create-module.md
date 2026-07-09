# Create Module Prompt

Use this prompt when asking Codex to create a future HRIS module.

```text
Create a new DepEd HRIS module in this Laravel 13 + React + Inertia project.

Module name:
[MODULE NAME]

Business purpose:
[PURPOSE]

DepEd users:
[REGION / DIVISION / DISTRICT / SCHOOL / IMPLEMENTING UNIT / HRMPSB / RECORDS / AUDITOR]

Policy context:
[DepEd policy area, CSC rule area, Data Privacy concern, records requirement]

Required workflow:
[Create, view, update, approve, reject, cancel, export, audit, etc.]

Before coding:
- Read AGENTS.md and relevant .codex/*.md files.
- Propose the module boundary, database model, permissions, audit events, validation rules, office scoping, and Pest test plan.
- Do not install packages.
- Do not change authentication flow.
- Do not implement unrelated HRIS modules.

When coding:
- Use Laravel conventions, Form Requests, policies or Spatie permissions, Eloquent relationships, transactions where needed, Activitylog, Inertia React, TypeScript, and Wayfinder route helpers.
- Preserve history for official HR actions.
- Protect sensitive data and 201 file references.
- Include Pest tests for authorization, validation, office scoping, state transitions, and audit logging.
```
