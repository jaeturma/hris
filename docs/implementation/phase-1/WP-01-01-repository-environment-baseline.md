# WP-01-01 Repository and Environment Baseline

## Execution record

| Field | Result |
|---|---|
| Inspection date | 2026-07-12 (Asia/Manila review date) |
| Repository | `D:\lara\www\hris` |
| Branch | `main` |
| Git state at start | Untracked Phase 0.10–0.14 documentation directories; no tracked modifications reported |
| Production-code changes | None |
| Recommendation | **READY FOR WP-01-02 WITH CONDITIONS** |

## Runtime and framework versions

| Component | Installed |
|---|---:|
| PHP | 8.3.16, Windows ZTS |
| Composer | 2.8.4 |
| Laravel Framework | 13.19.0 |
| Node.js / npm | 22.22.3 / 10.9.8 |
| Inertia Laravel / React adapter | 3.1.1 / 3.6.1 |
| React / React DOM | 19.2.7 / 19.2.7 |
| TypeScript | 5.9.3 |
| Vite | 8.1.4 |
| Tailwind CSS / Vite plugin | 4.3.2 / 4.3.2 |
| Pest / Laravel plugin | 4.7.5 / 4.1.0 |
| PHPUnit | 12.5.30 |
| PHPStan / Larastan | 2.2.5 / 3.10.0 |
| Pint | 1.29.3 |
| Spatie Permission / Activitylog | 8.3.0 / 4.12.3 |
| Fortify / Wayfinder | 1.37.2 / 0.1.20 |

The repository is the Laravel React starter-kit skeleton, not a separately versioned starter-kit package. Important additional direct packages include Laravel Passkeys, DOMPDF, Laravel Excel, Boost, Chisel, Tinker, Pail, Pao, Sail and IDE Helper. No package was installed or changed.

## Application structure

Backend currently contains one model (`User`), Fortify create/reset actions, profile/security controllers and requests, two custom middleware classes, and App/Fortify service providers. `app/Policies`, `app/Services`, `app/Events`, `app/Listeners`, and `app/Jobs` do not exist. There are nine migrations, one development seeder and one user factory. No HRIS business/domain module exists.

Frontend contains 12 pages, 8 layout files, 53 components and 8 hooks. It includes guest/auth pages, dashboard, profile/security/appearance settings, passkey and 2FA management, responsive sidebar/header shell primitives, Radix UI primitives, Wayfinder-generated actions/routes, strict TypeScript, Tailwind 4 and Inertia 3.

## Authentication and authorization

Fortify uses the `web` guard and email username. Registration, password reset, email-verification routes, confirmed 2FA, passkeys and password confirmation are enabled. Login includes remember-me. Rate limits are five/minute for login and 2FA, ten/minute for passkeys, six/minute for password updates/verification notification. Profile update/delete, password update, 2FA and passkey management exist; account deletion invalidates the session and regenerates the CSRF token.

Important condition: `User` uses `TwoFactorAuthenticatable` and `PasskeyAuthenticatable` but does not implement `MustVerifyEmail`. Therefore routes carrying `verified` middleware do not enforce verification for this model despite Fortify enabling the feature. This was not changed because authentication modification is prohibited in WP-01-01.

Spatie configuration and migrations exist, but `User` does not use `HasRoles`; no roles, permissions, Policies, Gates, role checks, permission middleware or authorization tests were found. Activitylog configuration/migrations exist, but no application logging behavior or `LogsActivity` model usage was found.

## Routes and middleware

Forty-five routes were listed: seven application-defined/non-vendor routes and 38 framework/package routes. Public routes include welcome/home, login, registration, reset-password, passkey login, health and selected package endpoints. Dashboard and several settings routes use `auth` plus `verified`; profile edit/update use `auth`; security settings require password confirmation; Fortify/passkey endpoints use guest/auth/password-confirm and rate-limit middleware as appropriate.

Laravel's configured web stack appends appearance, Inertia and preload-link middleware. Default web CSRF/session behavior remains active. No API route file is registered. No office-scope, role, permission or audit middleware exists. No duplicate named route was observed. Welcome and dashboard remain starter-kit placeholder pages.

## Database, migrations, seeders and factories

The active environment reports MySQL with database-backed cache, queue and session. Connectivity succeeded through `migrate:status`; all nine migrations are applied in three batches: users/cache/jobs, passkeys, two-factor columns, Spatie permission tables and Activitylog tables/event/batch UUID columns. No HRIS tables exist.

Tests use SQLite `:memory:` with array cache/session/mail and synchronous queue. `DatabaseSeeder` creates `test@example.com`; this is suitable only as development/demo behavior and is not production-safe. `UserFactory` produces synthetic verified users and optional unverified/2FA states. No destructive database command was run and no data/schema was modified.

`.env.example` still describes the generic Laravel SQLite/localhost baseline, while the active local environment uses MySQL and `hris.app`. It contains no populated secret. The real `.env`, vendor, node_modules and public build output are ignored by Git; `.env` is not tracked.

## Quality and test evidence

| Check | Command | Result |
|---|---|---|
| Laravel boot | `php artisan about` | Passed; local/debug enabled, URL `hris.app`, timezone UTC |
| Database | `php artisan migrate:status` | Passed; 9/9 migrations ran |
| Tests | `php artisan test --compact` | Passed: 39 tests, 136 assertions, 0 failed/skipped reported; 12.163 s test duration, 22.2 s command wall time |
| Static analysis | `composer types:check` | Passed; PHPStan level 7, 0 errors |
| PHP formatting | `composer lint:check` | Passed; custom `pint.json` uses Laravel preset |
| Composer manifest | `composer validate --no-check-publish` | Valid |
| TypeScript | `npm run types:check` | Passed |
| ESLint | `npm run lint:check` | Passed |
| Prettier | `npm run format:check` | Passed; all resource files matched |
| Production build | `npm run build` | Passed outside restricted sandbox; 2,296 modules, 29.84 s build |

The first sandboxed build failed with Windows `spawn EPERM` while loading Vite/Tailwind native dependencies. The approved unsandboxed rerun passed, so this is classified as an inspection-sandbox restriction, not an application defect. The build emitted a plugin-timing advisory: Inertia 52%, React Babel 23%, Laravel 11%, Tailwind generation 10%.

## Findings and classifications

| ID | Finding | Classification / effect |
|---|---|---|
| BL-01 | Official project name is “HRIS for DepEd”, but active `APP_NAME` reports `HRIS` and `.env.example` defaults to `Laravel`. | Configuration/documentation inconsistency; does not block WP-01-02. |
| BL-02 | `.env.example` defaults to SQLite/localhost instead of the documented Laragon MySQL/`https://hris.app` baseline. | Example-configuration drift; correct only through an approved baseline-remediation package. |
| BL-03 | Email verification is enabled and routes use `verified`, but `User` does not implement `MustVerifyEmail`. | Authentication behavior mismatch; requires WP-01-04/human decision before sensitive modules. |
| BL-04 | Application timezone is UTC; Phase 1 explicitly defers date/timezone convention to WP-02-02. | Expected unresolved convention; do not change in WP-01-01. |
| BL-05 | Permission/Activitylog packages and migrations exist but are not integrated into `User` or application behavior. | Expected Phase 1 foundation gap, not a defect; blocks business modules as designed. |
| BL-06 | `DatabaseSeeder` creates a fixed sample user. | Development-only behavior; must be separated from production-safe seeding before production use. |
| BL-07 | `npm list` reports three extraneous transitive/native packages (`@emnapi/wasi-threads`, `@napi-rs/wasm-runtime`, `@tybys/wasm-util`). | Dependency hygiene condition; build and checks pass; investigate without installing/upgrading in WP-01-03/06. |
| BL-08 | `public/storage` is not linked. | Informational; no current document feature. Resolve only when an approved storage use case requires it. |
| BL-09 | Phase 0.10–0.14 documentation is untracked on `main`. | Governance/Git baseline condition; human review/commit strategy required before later coding. |
| BL-10 | No office/organization ownership or scope exists; starter pages assume only authenticated user context. | Expected architecture gap; no business data may be introduced before EPIC-03/04. |

No tracked secret, destructive command, failing automated check, PHPStan suppression/baseline, custom authorization bypass or production-code change was found during this package.

## Recommended actions

1. Proceed to WP-01-02 to independently verify the backend quality tool contract and capture controlling commands.
2. Route BL-03 to WP-01-04; do not change Fortify/User behavior opportunistically.
3. Route BL-01/02/07 to conditional WP-01-06 only after explicit approval and after WP-01-02/03 evidence.
4. Resolve BL-04 in WP-02-02, not baseline remediation.
5. Keep BL-05/10 gated to their approved Phase 1 epics.
6. Classify the sample seeder before any production-safe seeder work.
7. Obtain human direction for committing the untracked architecture/backlog/implementation records before code work.

## Final recommendation

**READY FOR WP-01-02 WITH CONDITIONS**

The repository boots, connects to MySQL, passes all backend and frontend quality checks, and has no baseline defect that prevents backend quality-tool verification. Conditions BL-01–10 must remain visible and be routed to their approved packages; none authorizes an automatic fix.

