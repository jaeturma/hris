# Document Classification

## Purpose

Classify documents so access, retention, encryption, audit, notification, and sharing rules are clear before implementation.

| Classification | Description | Typical examples | Allowed viewers | Allowed editors | Download restrictions | Retention requirements | Audit requirements | Encryption expectations | Notification restrictions | External-sharing rules |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Public | Approved for public release. | Published vacancy notice. | Public/authorized users. | HR publisher. | Low. | Policy-configured. | Publish/release log. | Standard. | May include summary. | Allowed only after approval. |
| Internal | For DepEd internal use. | Office memo copy, internal checklist. | Authorized office users. | Owning office. | Permission-gated. | Policy-configured. | View/export where sensitive. | Standard/private. | Minimal details. | Restricted to authorized recipients. |
| Confidential | Contains personal or operational sensitive data. | Applicant documents, employee credentials. | Assigned HR/records/user owner. | Authorized HR/records. | Logged downloads. | Policy-configured. | View/download/verify. | Private storage; encryption expected. | Avoid sensitive details. | Requires authority. |
| Highly Confidential | High-risk personal or decision data. | Medical docs, performance ratings, payroll inputs. | Explicit permission only. | Restricted authorized users. | Strongly restricted. | Policy-configured; holds apply. | Log all access. | Encryption expected. | No SMS details. | Rare and approved only. |
| Restricted Personnel Record | Sensitive official personnel record. | 201 restricted docs, discipline references. | Records custodian, explicit HR/auditor. | Records custodian/restricted role. | Logged and purpose-bound. | Policy-configured. | Log preview/download/print/share. | Encryption expected. | Minimal notices only. | Requires formal basis. |
| HRMPSB Restricted | Selection deliberation/evaluation record. | Evaluation sheets, deliberation metadata, rankings before release. | Assigned cycle HRMPSB/HR/auditor. | Secretariat/evaluator as assigned. | Cycle-scoped and logged. | Policy-configured. | Log all access/actions. | Encryption expected. | Meeting/task notices only. | No external sharing unless authorized. |
| Applicant-Owned | Applicant's submitted records. | PDS, certificates, eligibility docs. | Applicant and assigned HR. | Applicant before lock; HR verifier. | Applicant own download; HR logged. | Policy-configured. | Upload/replace/verify/access. | Private. | Applicant-specific only. | Applicant may receive own records. |
| Employee Self-Service | Employee-visible own records. | Own service record copy, leave form copy. | Employee owner and authorized HR. | HR/records or employee where allowed. | Own download where allowed. | Policy-configured. | Download/release log. | Private. | Employee-specific only. | Employee own copy only. |
| Official Issuance | Policy/reference document. | DepEd Order, CSC issuance, Regional Memo. | Authorized users; public if published. | Policy admin. | Version-controlled. | Permanent/reference schedule. | Version and supersession log. | Standard/private as needed. | Policy update only. | Follow source publication rules. |
| Working Draft | Not official. | Draft report, draft form. | Creator/collaborators. | Creator/collaborators. | Limited. | Temporary retention. | Creation/finalization. | Private. | Avoid external notices. | Not shareable as official. |
| Final Official Record | Finalized official copy. | Released appointment, service record. | Authorized HR/records/subject where allowed. | No in-place edits. | Logged. | Policy-configured/permanent where required. | Release/access/version audit. | Encryption expected. | Minimal. | Official release process only. |
| Archived Record | In archive status. | Old service record packet. | Records custodian/auditor. | Records custodian. | Restricted. | Archive schedule. | Archive/restore/access log. | Archive encryption. | None unless action required. | By records authority only. |
| Superseded Record | Replaced but preserved. | Old policy version, corrected form. | Authorized users. | No editing. | Logged if sensitive. | Retain per schedule. | Supersession log. | Same as original. | Notify affected admins if needed. | Share only with context. |
| Temporary Record | Processing or staging file. | OCR staging, upload chunk. | System/authorized processor. | System. | Not user-downloadable. | Short configured period. | Processing log. | Private/quarantine. | None. | Never externally shared. |
| Policy Reference | Policy document used as basis. | DO, CSC MC, local memo. | Policy users, HR, auditors. | Policy admin. | Versioned reference download. | Retain as policy registry. | Register/supersede audit. | Standard/private. | Policy update notices. | Follow issuing authority rules. |

## Rule

Avoid generic permissions such as `view all documents`. Use explicit permissions aligned with classification, purpose, workflow assignment, office scope, and record ownership.
