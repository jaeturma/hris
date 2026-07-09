# UI Design System

The interface must be modern, accessible, responsive, and suitable for government HR operations. Avoid flashy consumer-style interfaces.

## Visual Direction

- Tone: professional, calm, clear, and data-focused.
- Density: optimized for HR staff handling many records.
- Shape: use modest radius, consistent spacing, and restrained borders.
- Motion: subtle and functional only.

## Color Palette

- Primary: deep government blue for navigation and primary actions.
- Secondary: neutral slate for shells, text, borders, and table structure.
- Success: green for approved or active states.
- Warning: amber for pending or needs-review states.
- Danger: red for rejected, cancelled, or destructive actions.
- Info: cyan or blue for informational states.

Colors must meet accessibility contrast requirements. Do not use color alone to communicate status.

## Typography and Spacing

- Use a clean sans-serif typeface already configured by the project.
- Use clear hierarchy: page title, section title, table heading, body, metadata.
- Use consistent spacing increments compatible with Tailwind utilities.
- Avoid oversized marketing-style headings in authenticated HR workflows.

## Components

- Cards: use for grouped data summaries, not for every page section.
- Forms: clear labels, required markers, validation messages, and logical grouping.
- Tables: sortable columns, filters, pagination, empty states, and compact rows.
- Buttons: primary, secondary, danger, ghost, and icon variants.
- Modals: confirmation or focused edits only; do not hide complex workflows inside modals.
- Drawers: useful for record previews, filters, and side details.
- Toasts: short operational feedback; do not use them for critical legal or HR decisions.
- Empty states: explain what is missing and what permitted users can do next.
- Loading skeletons: use for tables, cards, and dashboards to reduce layout shift.
- Status badges: include text labels such as `Pending`, `Approved`, `Rejected`, `Active`, `Separated`.
- Charts: use only when they clarify staffing, vacancies, leave, or workflow metrics.
- Dashboard widgets: concise, permission-aware, and office-scoped.

## Responsive Behavior

- Desktop layouts prioritize tables, filters, and side-by-side record details.
- Tablet layouts keep navigation and forms usable.
- Mobile layouts support review and light actions, but complex HR processing may remain desktop-optimized.

## Sensitive Data

Show only the minimum personal data required for the task. Hide or restrict 201 file, performance rating, recruitment, leave, and service record details unless the user has permission.
