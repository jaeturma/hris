# Folder Structure

Use Laravel conventions first. Add enterprise folders only when a real module needs them.

## Laravel Structure

Recommended future locations:

- `app/Models`: Eloquent models such as `Employee`, `PlantillaItem`, `ServiceRecord`.
- `app/Http/Controllers`: thin controllers that coordinate requests and Inertia responses.
- `app/Http/Requests`: Form Requests for validation and authorization checks.
- `app/Policies`: authorization policies for sensitive records.
- `app/Services`: reusable business services with multiple collaborators or workflows.
- `app/Actions`: single-purpose actions such as `ApproveAppointment` or `TransferEmployee`.
- `app/DTOs`: typed data transfer objects for complex validated inputs or external data.
- `app/Enums`: PHP enums for stable internal states such as workflow status.
- `app/Events`: domain events such as `AppointmentApproved`.
- `app/Listeners`: listeners for audit, notification, or asynchronous reactions.
- `app/Jobs`: queued work such as imports, exports, reports, and notifications.
- `app/Notifications`: Laravel notifications.
- `app/Mail`: mailables.
- `app/Support`: framework-neutral helpers that are project-specific.
- `app/Traits`: narrow reusable traits; avoid traits for business logic.
- `app/Helpers`: only when a helper is truly global and better than a service.

## Domain Organization

If modules become large, domain-oriented folders may be introduced under `app/Domains`, for example:

- `app/Domains/Employees`
- `app/Domains/Plantilla`
- `app/Domains/Recruitment`
- `app/Domains/PersonnelActions`
- `app/Domains/LeaveManagement`
- `app/Domains/Records`

Each domain may contain its own `Actions`, `Services`, `Data`, `Enums`, and `Queries`. Do not create domain folders before the module exists.

## React Structure

Recommended future locations:

- `resources/js/pages`: Inertia pages organized by module.
- `resources/js/components`: shared reusable UI components.
- `resources/js/layouts`: page layouts and shell components.
- `resources/js/features`: feature-specific UI pieces when a module grows beyond a page.
- `resources/js/hooks`: reusable React hooks.
- `resources/js/types`: shared TypeScript types.
- `resources/js/lib` or `resources/js/utils`: utilities such as formatting and filters.

Keep feature-specific components near their feature when they are not reusable. Move components to shared folders only after reuse is real.

## Why These Folders Exist

- Controllers keep HTTP concerns isolated.
- Requests keep validation consistent and testable.
- Policies and permissions keep sensitive access explicit.
- Services and actions keep HR workflows out of controllers.
- DTOs reduce array-shaped ambiguity.
- Enums prevent fragile string comparisons.
- Jobs keep slow government reports and imports reliable.
- React features keep large Inertia pages maintainable.
