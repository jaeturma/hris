# Approval Routing

## Purpose

Define reusable approval and review patterns for DepEd HR workflows.

| Pattern | Use Case | Risks | Audit Requirement | Recommended Implementation | Digital Signature |
| --- | --- | --- | --- | --- | --- |
| Sequential approval | Leave, personnel movement, service record release. | Bottlenecks and unavailable approvers. | Log each step, actor, timestamp, remarks. | Ordered workflow steps with deadline and delegation. | May apply to final approval. |
| Parallel review | Document screening, evidence review. | Conflicting findings. | Log reviewer assignments and results. | Multiple assigned step instances. | Usually no. |
| Any-one approval | Alternate authorized HR verifier. | Inconsistent handling. | Log assignment pool and acting approver. | First valid action completes step. | Possible when authority allows. |
| All-members approval | Committee sign-off requiring all members. | Delay if one member inactive. | Log each member action. | Step completes only after all required actions. | Possible. |
| Majority recommendation | HRMPSB recommendation where applicable. | Miscounting and recusal effects. | Log eligible members, votes/recommendation metadata, recusals. | Quorum-aware recommendation calculation after manual input. | Final report may be signed. |
| Quorum-based deliberation | HRMPSB meeting. | Invalid deliberation without quorum. | Log constitution, attendees, recusals, quorum check. | HRMPSB-specific workflow step. | Meeting record may be signed. |
| Secretariat validation | Documentary completeness and packet prep. | Secretariat appearing to decide merits. | Log validation basis and returned items. | Validation step before evaluation. | Usually no. |
| HRMPSB review | Recruitment, promotion, career progression. | Deliberation confidentiality. | Structured deliberation metadata and recommendation record. | Cycle-specific assignments. | Recommendation may be signed. |
| Appointing authority decision | Appointment approval or selection action. | Unauthorized action. | Log authority, capacity, date, decision. | Synchronous approval with authority check. | Yes, where supported. |
| Records release | Service record or 201 document release. | Privacy breach. | Log request, release, recipient, purpose. | Records officer step with access check. | Possible. |
| CSC submission | Appointment packet submission. | Missing documents or wrong cycle. | Log packet, submitter, date, result. | Appointment domain step. | Packet may be signed. |
| Return for compliance | Missing document or correction. | Ambiguous deficiency. | Require remarks and deficiency references. | Return transition with required remarks. | No. |
| Conditional approval | Approval subject to completion of stated items. | Hidden conditions. | Log condition text and completion proof. | State remains conditionally approved until cleared. | Possible final signature after clearance. |
| Delegated approval | Approver unavailable, delegated authority. | Unauthorized delegation. | Log delegation source, period, scope. | Delegation record checked at action time. | Yes, attributable to delegate capacity. |
| Acting authority approval | Acting official exercises authority. | Expired acting designation. | Log acting capacity and validity. | Temporary authority record with expiration. | Yes. |

## Rule

Human approvals must be synchronous, attributable, permission-checked, office-scoped, state-checked, policy-checked, and auditable.
