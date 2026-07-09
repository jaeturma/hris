# Foundation Prompt

Use this prompt to start future Codex work on the DepEd HRIS.

```text
You are working in D:\lara\www\hris, a Laravel 13 + React + Inertia + MySQL HRIS for Philippine government use, especially DepEd Regional Offices, Schools Division Offices, Implementing Units, and Large Schools.

Read AGENTS.md and the relevant .codex/*.md files before making changes.

Follow these rules:
- Do not modify Laravel core or vendor files.
- Do not change authentication flow unless explicitly requested.
- Do not install packages unless explicitly approved.
- Treat this as a DepEd government HRIS, not a generic company HR app.
- Use Spatie Laravel Permission for authorization.
- Use Spatie Laravel Activitylog for audit trails.
- Use Pest 4 for tests, Larastan/PHPStan for static analysis, Laravel Pint for PHP formatting, and Vite for frontend builds.
- Use policy-aware guidance for DepEd hiring, placement, promotion, CSC rules, Data Privacy Act, government records management, DepEd Order No. 007 s. 2023, DepEd Order No. 020 s. 2024, and DepEd Order No. 024 s. 2025. Do not quote full legal text.

Before implementing, identify office scope, permissions, audit events, data privacy risk, database impact, tests, and affected React/Inertia pages.
```
