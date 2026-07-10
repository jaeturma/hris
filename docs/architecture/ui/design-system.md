# Design System

## Purpose

Define a professional visual system suitable for DepEd HR operations, policy-sensitive workflows, and repeated daily use.

## Visual Identity

| Token | Recommendation | Usage |
| --- | --- | --- |
| Primary | Deep navy / DepEd blue | Sidebar, primary buttons, active navigation, key headers |
| Secondary | White / light gray | Page backgrounds, panels, table surfaces |
| Accent | Gold or warm yellow | Highlights, selected workflow step, important but non-danger prompts |
| Success | Green | Approved, active, complete |
| Warning | Amber | Pending, needs review, expiring, incomplete |
| Danger | Red | Rejected, cancelled, destructive action |
| Info | Blue / cyan | Informational notices, neutral status |

Avoid excessive gradients. Use solid colors, subtle borders, and restrained shadows. Do not use playful illustrations for operational screens.

## Typography

- Use clear sans-serif typography already configured in the project.
- Use compact headings inside dashboards, panels, sidebars, and cards.
- Avoid hero-scale typography in authenticated app screens.
- Keep labels direct: `Plantilla Item`, `Qualification Standard`, `HRMPSB Evaluation`, `Service Record`, `201 File`.

## Spacing and Shape

- Use consistent spacing based on Tailwind utility scale.
- Prefer `gap` between siblings when implemented.
- Use compact 8px or smaller radius unless existing components require otherwise.
- Avoid nested cards. Use panels, table sections, tabs, or full-width bands instead.

## Component Standards

| Component | Standard |
| --- | --- |
| Cards | Use for repeated summaries or dashboard widgets only. |
| Forms | Clear labels, required markers, help text, validation messages, and grouped sections. |
| Tables | Dense, scannable, sortable, filterable, paginated, and export-aware. |
| Buttons | Clear visual hierarchy: primary, secondary, danger, ghost, icon. |
| Badges | Text plus color; never color alone. |
| Modals | Confirm or focus a small task; avoid complex workflow editing in modals. |
| Drawers | Good for filters, previews, document details, or audit panels. |
| Toasts | Short feedback only; not for critical policy decisions. |
| Skeletons | Use for tables, dashboards, and record summaries to avoid layout shift. |

## Status Labels

Use consistent labels: `Draft`, `Submitted`, `For Screening`, `Qualified`, `Disqualified`, `For HRMPSB Review`, `Ranked`, `Recommended`, `Approved`, `Returned`, `Rejected`, `Released`, `Archived`.

## Dark Mode

If dark mode remains enabled in the application, all future UI must include matching dark variants. Sensitive status colors must remain distinguishable in both light and dark themes.
