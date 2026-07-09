# UI Rules

The interface must feel like a professional government HR operations system for DepEd, not a marketing site or generic admin template.

## Product Character

- Prioritize clarity, density, auditability, and repeated daily use.
- Use official HR terminology in visible labels.
- Keep visual design restrained and accessible.
- Avoid decorative layouts that reduce scanning speed.
- Avoid landing-page composition for authenticated app screens.

## Inertia React

- Build actual workflows as first-class pages.
- Use typed props and existing component patterns.
- Use Wayfinder route helpers for Laravel route calls.
- Keep forms accessible, keyboard-friendly, and explicit about required fields.
- Use server-side validation as the source of truth.

## Information Architecture

Future navigation should account for Dashboard, Employees, Plantilla, Recruitment and HRMPSB, Appointments and Personnel Actions, Service Records, Leave Management, Performance Ratings, 201 Files, Reports, Administration, and Audit Trail.

Do not create these modules until requested.

## Layout Rules

- Make tables and lists efficient for HR staff reviewing many records.
- Provide filters for office scope, status, position title, salary grade, item number, and date ranges where relevant.
- Show status and effective dates clearly.
- Use confirmation dialogs for irreversible or official actions.
- Make export actions visually distinct and permission-aware.

## Accessibility

- Use semantic controls.
- Maintain sufficient contrast.
- Do not rely on color alone for status.
- Ensure focus states are visible.
- Keep forms usable with keyboard navigation.

## Sensitive Data Display

- Show the minimum personal data needed for the task.
- Avoid exposing 201 file details, performance ratings, or personal identifiers in broad lists unless necessary.
- Hide or disable actions the user cannot perform, but still enforce permissions on the server.
