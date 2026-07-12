# UI Shell and Design-System Implementation Plan

## Sequence

1. Confirm existing React 19/Inertia v3/Tailwind patterns during WP-1.
2. Freeze tokens: DepEd/navy blue, white/light gray, restrained gold accent, semantic statuses, typography, spacing and focus treatment.
3. Build/test primitives: link/button, field/error summary, alert/badge, dialog, loading/empty/error/forbidden states.
4. Build responsive authenticated shell: skip link, sidebar/drawer, top bar, page header and breadcrumbs.
5. Integrate server-authorized office switcher, role/context summary and permission-aware navigation.
6. Add table/filter/pagination patterns and audit/workflow history presentation before business screens.

The switcher displays only assigned scopes and cannot grant access. Navigation visibility is usability, not authorization. Inertia props are explicit/minimal/typed; frontend calls use Wayfinder-generated routes when future Laravel routes are introduced.

Acceptance requires keyboard navigation, focus management, screen-reader landmarks/labels, error announcement, contrast, responsive behavior, loading/empty/error states, no color-only meaning, typed props, successful build and security review of context switching. C-13 must pass before shell completion.

