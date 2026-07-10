# Forms and Validation

Forms must be clear, accessible, policy-aware, and safe for sensitive HR data.

## Form Layout

- Use sectioned forms for long HR records.
- Group related fields: identity, office scope, position, documents, evaluation, approvals.
- Use clear labels and required markers.
- Place help text near policy-sensitive fields.
- Keep primary action at the bottom and sticky only when useful.
- Use save draft where workflows are long.

## Validation UX

- Server validation is the source of truth.
- Show inline field errors and a summary at the top for long forms.
- Preserve user input after validation failures.
- Use plain language messages.
- Avoid exposing policy internals or sensitive data in errors.

## Multi-Step Forms

Use stepper patterns for:

- Vacancy creation.
- Applicant application.
- Documentary requirement submission.
- Promotion application.
- Reclassification request.
- Competency assessment.
- IDP creation.

Each step should show completion status, missing fields, and save state.

## Document Upload UI

Document upload screens should show:

- Required document list.
- Accepted file types and max size.
- Upload status.
- Verification status.
- Replacement history where authorized.
- Sensitive document warning.

Do not expose storage paths. Upload, replace, verify, reject, and download actions must be permission-aware and logged.

## Approval Forms

Approval UI should include:

- Record summary.
- Policy/reference context.
- Current workflow state.
- Required evidence checklist.
- Remarks field.
- Approve, return, reject, or cancel actions based on permission.
- Confirmation dialog for final actions.
