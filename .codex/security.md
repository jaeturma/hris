# Security, Privacy, and Audit Rules

This HRIS will handle sensitive government personnel records. Security must be designed into every feature.

## Access Control

- Use Spatie Laravel Permission for roles and permissions.
- Enforce authorization in Laravel, not only in React.
- Scope permissions by office where needed: Region, Division, District, School, or Implementing Unit.
- Use least privilege defaults.
- Separate view, create, update, approve, cancel, export, and audit permissions.
- Never assume a logged-in user can access all employees.

## Suggested Role Families

Actual roles must be confirmed before implementation, but future designs should account for regional HR administrator, division HR administrator, school or implementing-unit HR staff, HRMPSB member, approving authority, records officer, read-only auditor, and system administrator.

## Data Privacy

- Treat employee profiles, 201 files, leave records, performance ratings, recruitment records, and service records as sensitive personal information.
- Apply data minimization.
- Mask or omit personal data in lists when full details are unnecessary.
- Restrict exports and downloads.
- Avoid exposing IDs that allow easy enumeration where the route can be guessed.
- Do not place sensitive data in browser console logs, URLs, exception messages, or activity descriptions.

## Audit Trail

- Use Spatie Laravel Activitylog for significant actions.
- Log record creation, update, approval, rejection, cancellation, export, and permission-sensitive viewing where appropriate.
- Include actor, subject, office scope, action, timestamp, and changed fields when safe.
- Do not log full documents or excessive personal data.
- Audit records must be readable by authorized auditors only.

## Authentication

- Do not change the authentication flow unless explicitly requested.
- Keep password, passkey, email verification, and other auth behavior aligned with Laravel Fortify and project starter-kit conventions.

## Government Records

- Design with records retention and traceability in mind.
- Avoid hard deletion of official HR records.
- Provide correction workflows instead of silent overwrites for official records.
- Exports and reports must identify generation time, requesting user, and office scope when implemented.
