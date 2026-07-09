# Git Workflow

Use a disciplined workflow so government HR changes remain traceable.

## Branch Naming

- `docs/project-standards`
- `feature/employees`
- `feature/plantilla-management`
- `fix/appointment-authorization`
- `refactor/service-record-actions`
- `chore/dependency-maintenance`

Use lowercase words separated by hyphens.

## Commit Messages

Use clear, scoped commit messages:

- `docs: add project standards`
- `feature: add employee profile planning`
- `fix: enforce appointment approval permission`
- `test: cover service record authorization`
- `refactor: simplify plantilla assignment action`

Each commit should represent one coherent change.

## Pull Request Expectations

Every pull request should include:

- Purpose
- Scope
- Screenshots for UI changes
- Database changes, if any
- Permissions affected
- Audit events affected
- Data privacy considerations
- Tests and checks run
- Policy assumptions or references

## Code Review Checklist

- Does it follow DepEd terminology?
- Is office scope enforced?
- Are permissions and policies correct?
- Are sensitive records protected?
- Are audit events present where needed?
- Are database constraints and indexes appropriate?
- Are Pest tests meaningful?
- Does the UI remain accessible and government-appropriate?

## Release Tags and Versioning

Use semantic versioning once releases begin:

- `v0.x`: internal development
- `v1.0.0`: first production-ready baseline
- Patch releases for fixes
- Minor releases for backward-compatible features
- Major releases for breaking changes

Document release notes with migration, permission, audit, and data privacy impacts.
