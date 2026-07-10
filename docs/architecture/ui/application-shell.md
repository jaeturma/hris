# Application Shell

## Purpose

Define the common authenticated shell for daily HR operations.

## Main Layout

- Fixed or sticky sidebar on desktop.
- Top bar with page context, office context, notifications, quick actions, and user menu.
- Main content area optimized for tables, workflow queues, forms, and reports.
- Breadcrumbs below the top bar or inside the page header.
- Optional right-side drawer for filters, audit history, document preview, or workflow details.

## Sidebar Navigation

- Group navigation by HR domain, not by technical module.
- Show only groups the user has permission to access.
- Keep icons simple and familiar.
- Support collapsed desktop sidebar.
- On tablet/mobile, use an off-canvas navigation drawer.

## Header / Top Bar

Include:

- Current page title or module.
- Office context switcher if the user has more than one authorized scope.
- Notification area.
- Quick actions menu.
- User profile menu.

## Breadcrumbs

Use breadcrumbs for deep workflows:

`Recruitment & Selection > Vacancies > Teacher I > Applications > Applicant Name`

Do not use breadcrumbs as a substitute for clear page headings.

## Office Context Switcher

Show only when applicable. It must:

- Display current office scope.
- Include Region, Division, District, School, Implementing Unit, or Office / Station as relevant.
- Never expand access beyond server-authorized scopes.
- Affect dashboards, lists, reports, and quick actions.

## Notification Area

Notifications should include:

- Pending approvals.
- Returned workflows.
- Expiring publication windows.
- Missing documents.
- HRMPSB assignment reminders.
- Document verification tasks.

## Quick Actions

Quick actions must be permission-aware. Examples:

- Create vacancy.
- Register applicant.
- Upload document.
- Start promotion cycle.
- Generate DTR.
- View audit log.

## User Profile Menu

Include profile, office scope, role summary, account/security settings, and sign out. Do not expose role management unless authorized.
