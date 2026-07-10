# Document Lifecycle

## Purpose

Define standard document states and controls. Not every document uses every state.

| State | Meaning | Allowed actions | Authorized actors | Required metadata | Audit requirement | Editability | Download behavior | Transition guards | Notification impact |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Draft | Created but not submitted. | Edit, delete draft if allowed, submit. | Creator/authorized HR. | title, type, owner, draft flag. | Draft creation/update if sensitive. | Editable. | Usually restricted. | Required fields complete. | None or draft reminder. |
| Uploaded or Generated | File exists in storage or generated output. | Review, classify, submit. | Uploader/generator/HR. | storage ref, hash, filename, source. | Upload/generation log. | Metadata editable; file immutable as version. | Permission-gated. | Virus/security checks. | Optional. |
| Submitted | Sent for intake/review. | Receive, return, cancel if allowed. | Applicant/employee/HR. | submitted_by, submitted_at, workflow. | Submission log. | Locked except replacement rules. | Owner/HR only. | Submission window and required docs. | Receipt notice. |
| Received | Acknowledged by office. | Assign verifier, review. | HR/records. | received_by, office, date. | Receipt log. | Not file-editable. | HR/owner rules. | Office scope valid. | Intake notice. |
| Under Verification | Being checked. | Verify, return, reject. | Verifier/records/HR. | verifier, method, policy basis. | Verification action log. | Not file-editable. | Restricted if sensitive. | Assigned verifier. | Task/reminder. |
| Verified | Accepted as valid evidence. | Use in workflow, expire, supersede. | Verifier/records. | verified_by, date, method. | Verification log. | Immutable verification decision. | Permission-gated. | Verification complete. | Result notice. |
| Returned for Compliance | Deficiency identified. | Replace, resubmit, cancel. | Submitter/HR. | deficiency remarks. | Return log. | New version allowed. | Submitter/HR. | Required remarks. | Deficiency notice. |
| Approved | Approved as workflow output or supporting record. | Sign, release, finalize. | Approver. | approval record. | Approval log. | No file overwrite. | Permission-gated. | Approval authority. | Result notice. |
| Signed | Signature applied or signature metadata recorded. | Validate, release, archive. | Authorized signatory/system validator. | signer, method, certificate/timestamp/hash. | Signature log. | Immutable. | Logged. | Authorized human signing action. | Signature complete. |
| Released | Official copy made available. | Download, print, archive, supersede. | Records/HR. | release date, recipient. | Release/access log. | Immutable released version. | Logged. | Final approval/signature if required. | Release notice. |
| Finalized | Official and locked. | Supersede, archive, place hold. | Records/authorized HR. | finalized_at, finalizer. | Finalization log. | Immutable. | Logged if sensitive. | Required approvals complete. | Optional. |
| Active Record | Current official record. | Use, reference, supersede. | Authorized users. | active flag, retention start. | Access/action log. | Immutable file; metadata controlled. | Permission-gated. | Finalized. | Workflow dependent. |
| Superseded | Replaced by newer version. | View, archive, retain. | Authorized users. | superseded_by, reason. | Supersession log. | Immutable. | Context warning. | New version approved. | Admin notice if needed. |
| Archived | Moved to archive status/storage. | Restore if allowed, retain, hold. | Records custodian. | archive ref, archived_by. | Archive log. | Immutable. | Restricted. | Retention/archive rule. | None or records notice. |
| Retained | Held under retention schedule. | Review, hold, dispose if allowed. | Records custodian. | retention rule, review date. | Retention review log. | Immutable. | Restricted. | Schedule applies. | Retention due notice. |
| Disposed | Legally disposed if permitted. | View disposition certificate only. | Records custodian/auditor. | disposition certificate, authority. | Immutable disposition log. | File unavailable except certificate. | No file download unless archive copy lawfully retained. | Approval, no holds, schedule valid. | Disposition completion notice. |

## Rule

No failure, regeneration, correction, or signature process should silently replace or delete an official file.
