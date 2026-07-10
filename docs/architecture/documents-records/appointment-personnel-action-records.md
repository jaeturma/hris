# Appointment and Personnel Action Records

## Purpose

Define records for appointment, CSC action, personnel movement, reclassification effects, retitling, separation, and retirement.

## Record Types

Appointment form, Position Description Form, Oath of Office, Assumption to Duty, medical certification, certification of publication, qualification certification, CSC submission record, CSC action, return-for-compliance notice, validation or invalidation record, promotion, transfer, reassignment, detail, designation, reclassification, retitling, separation, and retirement.

## Relationship Model

| Layer | Meaning |
| --- | --- |
| Structured personnel action | The transactional source of truth. |
| Generated form | Document output from structured record and template version. |
| Signed document | Official file with signature metadata. |
| Released copy | Copy made available to authorized recipient. |
| Archived official copy | Long-term retained official version. |

## Rules

- Appointment and CSC records are restricted personnel records.
- Returned CSC actions must not overwrite original submission packets.
- Corrected appointment documents become new official versions.
- Personnel movement documents must link to service-record updates.
- Retitling and reclassification records must preserve policy version and item/position impact.
