# Phase 1 Test Coverage Matrix

Legend: R required, C conditional/applicable, — not applicable. Individual packages specify exact cases.

| Epic | Unit | Feature | Auth | Scope | Validation | DB | Seeder | Frontend | A11y | Regression | Security | Manual |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 01 Baseline | C | R | C | — | — | — | — | R | C | R | R | R |
| 02 Conventions | R | C | — | — | R | C | — | C | — | R | C | R |
| 03 Organization | R | R | R | R | R | R | R | R | R | R | R | R |
| 04 Office Scope | R | R | R | R | R | R | C | R | R | R | R | R |
| 05 Authorization | R | R | R | R | R | R | R | C | C | R | R | R |
| 06 Audit | R | R | R | R | R | R | — | R | C | R | R | R |
| 07 References | R | R | R | C | R | R | R | C | C | R | R | R |
| 08 Policy Registry | R | R | R | R | R | R | C | R | R | R | R | R |
| 09 Shell | C | R | R | R | R | — | — | R | R | R | R | R |
| 10 Hardening | R | R | R | R | R | R | R | R | R | R | R | R |

Automated negative tests are mandatory for unauthorized, wrong-office, stale context, expired delegation, administrator without business authority, hierarchy restructuring, immutable history and audit completeness. WP-1 verifies the actual Pest/PHPUnit, PHPStan/Larastan, Pint, TypeScript, ESLint/Prettier and build commands.

