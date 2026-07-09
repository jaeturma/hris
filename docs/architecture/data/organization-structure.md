# Organization Structure Data

## Purpose

Model DepEd office hierarchy and assignment scope for Regional Offices, Schools Division Offices, Districts, Schools, Implementing Units, offices, office units, and stations.

## Proposed Tables

| Table name | Description | Key fields | Parent/dependent tables | Seeder needed? | Audit sensitivity |
| --- | --- | --- | --- | --- | --- |
| `regions` | DepEd regional offices. | `id`, `code`, `name`, `address`, `is_active` | Parent of `divisions` | yes | low |
| `divisions` | Schools Division Offices. | `id`, `region_id`, `code`, `name`, `address`, `is_active` | Parent `regions`; parent of `districts`, `schools` | yes | low |
| `districts` | District groupings under a division. | `id`, `division_id`, `code`, `name`, `is_active` | Parent `divisions`; parent of `schools` | yes | low |
| `schools` | School records. | `id`, `division_id`, `district_id`, `school_id_number`, `name`, `school_type`, `is_active` | Parent `divisions`, `districts`; used by employees and vacancies | yes | medium |
| `implementing_units` | Implementing Units / Large Schools with delegated functions. | `id`, `school_id`, `division_id`, `code`, `name`, `delegation_type`, `is_active` | Parent `schools`, `divisions` | yes | medium |
| `offices` | Offices within region, division, school, or IU context. | `id`, `officeable_type`, `officeable_id`, `code`, `name`, `is_active` | Polymorphic parent or scoped office hierarchy | yes | medium |
| `office_units` | Units or sections under an office. | `id`, `office_id`, `code`, `name`, `parent_unit_id`, `is_active` | Parent `offices`; self-parent | yes | medium |
| `stations` | Official station or assignment location. | `id`, `region_id`, `division_id`, `school_id`, `implementing_unit_id`, `office_id`, `station_code`, `name`, `is_active` | Used by `employee_assignments`, `employee_movements` | yes | medium |

## Main Fields

Use official codes where available, names, active flags, parent IDs, address/contact metadata, and effective dates when office structure changes.

## Relationships

Regions own divisions; divisions own districts and schools; schools may own implementing units; offices and units provide administrative structure; stations represent official assignment locations.

## Indexing Considerations

Index official codes, parent IDs, `is_active`, and common reporting combinations such as `region_id + division_id`, `division_id + district_id`, and `school_id + is_active`.

## Data Ownership

Owned by system administrators with HR governance oversight. Regional or division administrators may maintain their own subordinate offices if authorized.

## Data Visibility Rules

General office names are broadly visible. Administrative metadata and inactive structure history should be visible only to authorized HR/admin users.

## Audit Requirements

Audit office hierarchy changes because they affect permissions, reports, employee assignments, vacancies, and service records.

## Seeder Requirements

Seed verified official region/division/school/IU masterlists only. Allow controlled imports for large school lists.

## Notes Before Migration Creation

Decide whether `offices` should use polymorphic ownership or explicit nullable scope columns. Confirm official codes and hierarchy source.
