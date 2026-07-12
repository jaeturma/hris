# 02 Policy Registry and Versioning

## Purpose

Define the centralized registry for DepEd, CSC, Regional, Division, local, and internal HR policy sources.

## Policy Categories

| Category | Examples | Owner | Notes |
| --- | --- | --- | --- |
| National law/regulation | Data Privacy, records requirements | Policy/legal owner | Reference only unless structured into rules. |
| CSC issuance | CSC MC, CSC Resolution, ORAOHRA | HR policy owner | Provides government-wide appointment and HR rules. |
| DepEd national issuance | DepEd Orders, DepEd Memoranda | HR policy owner | Primary for DepEd workflows. |
| Regional Memorandum | RO implementing memo | Regional HR | May clarify or implement; cannot override higher mandatory rule. |
| Division Memorandum | SDO implementing memo | Division HR | Scope-limited implementation. |
| Agency MSP | Merit Selection Plan | HR leadership | Versioned and linked to HRMPSB/selection workflows. |
| PRIME-HRM/PRAISE/SPMS | Program policies | HR owners | Supports compliance and strategic HRM. |
| Internal procedure | SOP/checklist | Process owner | Must remain subordinate to policy. |
| Retention/privacy policy | Retention schedule, privacy notices | Records/DPO | Drives document handling. |

## Policy Record Required Fields

Issuing authority, issuance type, issuance number, series year, official title, subject, description, source document, official publication/reference, date issued, date approved, effective date, expiration date, supersession status, amended policies, superseding policy, applicable offices, applicable personnel groups, applicable position groups, applicable transaction types, legal/administrative basis, responsible policy owner, and verification status.

## Policy Statuses

| Status | Meaning |
| --- | --- |
| Draft | Registered but incomplete. |
| Pending verification | Awaiting policy owner review. |
| Verified | Source confirmed but not active. |
| Approved | Authorized for activation/configuration. |
| Active | Can be used for new transactions. |
| Suspended | Temporarily not usable pending review/directive. |
| Superseded | Replaced by later policy/version. |
| Archived | Retained for historical reference. |
| Rejected | Not approved as a valid policy source. |
| Under review | Legal/admin review is active. |

## Policy Version Statuses

Draft, Pending Configuration, Pending Approval, Approved, Active, Superseded, Suspended, Archived, Corrected.

## Version Rules

- A policy is not active merely because it was uploaded.
- Activation requires authorized human verification and approval.
- Once used by an official transaction, the version must not be destructively edited.
- Corrections create a new version or authorized correction record.
- Version records preserve effective-from, effective-to, source version, structured rule set, applicability conditions, change summary, approved-by, activation timestamp, and validation notes.
