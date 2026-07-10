# Responsive Design

The HRIS is desktop-first for HR operations but must remain usable on tablets and mobile devices.

## Desktop

Primary layout:

- Persistent sidebar.
- Top bar with office context.
- Dense tables.
- Side-by-side detail panels.
- Drawers for filters, audit history, and document preview.

Use desktop for complex workflows such as HRMPSB review, ranking, appointment packets, competency mapping, and payroll preparation.

## Tablet

Tablet layout:

- Collapsible sidebar or navigation drawer.
- Tables may reduce columns.
- Filters move into a drawer.
- Workflow panels stack vertically.
- Approval actions remain visible near the record summary.

## Mobile

Mobile layout:

- Bottom or drawer navigation for limited self-service workflows.
- Card/list views instead of dense tables.
- Single-column forms.
- Sticky primary action only when it does not cover content.
- Prioritize employee, applicant, approval review, leave, document upload, and notification flows.

Avoid forcing complex ranking, HRMPSB deliberation, payroll export, or wide audit tables into mobile-only workflows.

## Breakpoint Behavior

- Sidebar collapses before content becomes cramped.
- Tables switch to fewer columns or card rows.
- Filters move from inline panel to drawer.
- Breadcrumbs truncate middle segments.
- Long labels wrap rather than overflow.

## Performance

Use loading skeletons for dashboards and tables. Avoid layout shifts from late-loading counts, filters, or buttons.
