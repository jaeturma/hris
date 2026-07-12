# UI/UX and Accessibility Gap Review

| Risk | Required UI behavior/test | Severity / gate |
|---|---|---|
| wrong/stale office context | persistent office/acting context, confirmation on context-sensitive action, server rejection and refresh | High; WP-9/security |
| hidden validation/error | field association + summary + focus/announcement; server errors preserved | Medium |
| inaccessible approval/dialog | keyboard, focus trap/return, semantic label, screen-reader status | High for critical action |
| accidental destructive/final action | consequence, record/office context, reason and explicit confirmation | High |
| restricted record ambiguity | classification/restriction indicator without leaking content | High |
| draft/finalized/advisory confusion | distinct text/state, not color alone; finalized immutable and AI clearly advisory | High by module |
| table/filter/pagination access | captions/headers, control labels, result count/focus and mobile representation | Medium |
| acting/delegated authority hidden | display capacity, scope and expiry during action | High |

Phase 0.12 covers shell primitives but should add acting capacity, stale context, restricted-record and draft/final/advisory states to WP-9 acceptance. C-13 remains open because WCAG-oriented manual and automated protocols are not approved.

