# ADR-020: Independent Gap Gates and Work-Package Blocking

- Status: Accepted in Phase 0.13, subject to human Phase 1 approval
- Date: 2026-07-12

## Context

Readiness planning does not itself resolve architecture, policy, security or data gaps. A single unresolved issue should block the scope it endangers without automatically authorizing or stopping unrelated read-only validation.

## Decision

Phase 0.13 is independent validation. Current Critical gaps block all affected implementation; High gaps block affected work packages; intentional deferrals require a named register, trigger and owner. Phase 1 remains foundation-only. Appointment truth is owned by Appointment and Personnel Action. WP-3 must split before development approval, and bootstrap audit must protect privileged foundation mutations.

## Consequences

WP-1 may be authorized only through its entry gates. Every later work package is revalidated against the gap register, traceability, tests and human approvals. Architecture changes discovered during implementation follow ADR/change control before work resumes.
