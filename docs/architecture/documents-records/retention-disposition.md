# Retention and Disposition

## Purpose

Define retention and disposition controls for government HR records.

## Required Data

Records series, policy source, retention schedule version, retention start event, active retention period, archive period, permanent retention, disposition eligibility, legal hold, audit hold, investigation hold, disposition approval, destruction method, transfer to archive, disposition certificate, and cancellation of disposition.

## Rules

- Retention must be policy-driven.
- Do not hardcode retention periods until validated against official schedules.
- The system must not automatically destroy official government records.
- Disposition requires authorized human approval.
- Holds suspend disposition.
- Records linked to unresolved cases or audits must not be disposed.
- Disposition history must be immutable.
- Disposition cancellation must record reason and authority.

## Disposition Flow

1. Identify disposition eligibility from schedule.
2. Check legal, audit, investigation, and workflow holds.
3. Route to records custodian and approval authority.
4. Approve transfer, archive, or lawful destruction if permitted.
5. Record disposition certificate and evidence.
6. Preserve metadata and audit history.
