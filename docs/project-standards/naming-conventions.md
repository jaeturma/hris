# Naming Conventions

Names must be consistent, searchable, and grounded in DepEd HR terminology.

## Laravel Classes

| Type | Correct | Incorrect |
| --- | --- | --- |
| Model | `Employee`, `PlantillaItem`, `ServiceRecord` | `Emp`, `ItemData`, `RecordInfo` |
| Controller | `EmployeeController`, `PlantillaItemController` | `Employees`, `EmployeeManagerController` |
| Form Request | `StoreEmployeeRequest`, `UpdatePlantillaItemRequest` | `EmployeeRequest`, `SaveRequest` |
| Policy | `EmployeePolicy`, `ServiceRecordPolicy` | `EmployeeAccess`, `RecordAuth` |
| Service | `ServiceRecordService`, `PlantillaAssignmentService` | `ServiceHelper`, `ProcessService` |
| Action | `ApproveAppointment`, `TransferEmployee` | `DoApproval`, `MovePerson` |
| Event | `AppointmentApproved`, `EmployeeTransferred` | `AppointmentEvent`, `ActionDone` |
| Job | `GenerateServiceRecordPdf`, `ImportPlantillaItems` | `PdfJob`, `ImportJob` |
| Notification | `AppointmentApprovedNotification` | `NotifyAppointment` |
| Mailable | `PersonnelActionSummaryMail` | `EmailSummary` |
| Resource | `EmployeeResource`, `PlantillaItemResource` | `EmployeeJson`, `ItemOutput` |
| Seeder | `RolePermissionSeeder`, `OfficeHierarchySeeder` | `RolesSeeder2`, `DataSeeder` |

Use singular model names and plural table names. Use clear DepEd domain words such as `Region`, `Division`, `District`, `School`, `ImplementingUnit`, `Employee`, `PlantillaItem`, `PositionTitle`, `SalaryGrade`, `ItemNumber`, `Appointment`, `Promotion`, `Transfer`, `Separation`, `ServiceRecord`, `LeaveApplication`, `PerformanceRating`, and `Hrmpsb`.

## React and TypeScript

| Type | Correct | Incorrect |
| --- | --- | --- |
| Component | `EmployeeStatusBadge`, `OfficeScopeSelect` | `Badge1`, `SelectBox` |
| Page | `Employees/Index`, `PlantillaItems/Show` | `EmployeesPage2`, `MainItems` |
| Layout | `AuthenticatedLayout`, `RecordsLayout` | `MainLayout2` |
| Hook | `useOfficeScope`, `useEmployeeFilters` | `useStuff`, `useData` |
| Utility | `formatSalaryGrade`, `parseItemNumber` | `helper1`, `doFormat` |
| Type | `EmployeeSummary`, `OfficeScope` | `Data`, `Obj` |

React components use PascalCase. Hooks use camelCase and start with `use`. Utility functions use camelCase. Types and interfaces use PascalCase.

## Database

- Tables: plural snake_case, for example `employees`, `plantilla_items`, `service_records`.
- Pivot tables: singular model names in alphabetical order, for example `employee_role` only when not using Spatie tables; otherwise follow package conventions.
- Foreign keys: singular table name plus `_id`, for example `employee_id`, `division_id`, `plantilla_item_id`.
- UUID columns: use `_uuid` suffix only when the column stores a UUID separate from the primary key.
- Indexes: use descriptive names when Laravel defaults become unclear, for example `employees_division_status_index`.

## Routes

Route names use dot notation and plural resources:

- Correct: `employees.index`, `employees.show`, `plantilla-items.assign`, `appointments.approve`
- Incorrect: `employeeList`, `approveAppointmentNow`, `items.do`

## Permissions and Roles

Permissions use plural resource and action:

- Correct: `employees.view`, `employees.create`, `appointments.approve`, `service-records.export`
- Incorrect: `view employee`, `canApprove`, `admin.employee.all`

Role names should be human-readable and office-aware when needed:

- Correct: `Regional HR Administrator`, `Division Records Officer`, `School HR Staff`, `HRMPSB Member`, `Read-only Auditor`
- Incorrect: `Super User 2`, `HR`, `Approver`
