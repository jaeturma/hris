# Document Audit Trail

## Purpose

Define auditable document actions and required audit fields.

## Auditable Actions

Upload, replace with new version, submit, receive, verify, reject, return, approve, sign, validate signature, release, download, print, share, archive, restore, place on hold, remove hold, mark for disposition, approve disposition, dispose, and transfer to archive.

## Required Audit Fields

Actor, action, document, version, timestamp, office context, workflow context, reason, previous status, new status, device or IP metadata where appropriate, and delegated or acting capacity.

## Rules

- Restricted-record preview and download require access logs.
- Official lifecycle decisions require structured history, not only generic activity logs.
- Audit records must avoid storing full document contents or unnecessarily sensitive remarks.
- Audit exports are themselves sensitive and must be logged.
