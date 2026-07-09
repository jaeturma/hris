# API Guidelines

The initial application uses Inertia, but future APIs must follow these standards.

## Versioning

- Prefix public APIs with a version such as `/api/v1`.
- Avoid breaking response shapes within the same version.
- Document deprecations before removal.

## Responses

- Use Laravel API Resources for structured responses.
- Return consistent metadata for pagination and filters.
- Do not expose sensitive personal data by default.
- Include office scope only when authorized and useful.

## Validation and Errors

- Use Form Requests for validation.
- Return standard validation error responses.
- Use clear error codes or messages without exposing sensitive internals.
- Never leak stack traces, SQL, secrets, or private HR data.

## Pagination, Filtering, and Sorting

- Paginate all large lists.
- Whitelist filterable and sortable fields.
- Support common HR filters such as office scope, status, position title, salary grade, item number, and date range.
- Apply authorization before returning filtered data.

## Authentication and Authorization

- Use the project-approved authentication method when APIs are introduced.
- Do not weaken existing Fortify authentication.
- Enforce Spatie permissions and policies server-side.
- Log sensitive API exports and bulk access.

## Compatibility with Inertia

Do not create duplicate API behavior for an Inertia page unless a separate API client or integration requires it.
