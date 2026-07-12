# 21 Events, Workflows, and Integration

## Purpose

Align policy, AI, analytics, and decision-support events with Phase 0.8.

## Event Catalog

| Event | Producer | Consumers | Payload | Sensitivity | Idempotency | Audit | Retry | Failure handling | Notification |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| PolicyRegistered | Policy Registry | Policy reviewers | policy_id, actor, office | High | policy_id | Required | No automatic business retry | Return for correction | Reviewer task |
| PolicyVerified | Policy owner | Approvers | policy_id, verification_id | High | verification_id | Required | No | Reopen review | Approval task |
| PolicyApproved | Approver | Activation workflow | policy_id, approval_id | Restricted | approval_id | Required | No | Manual correction | Activation task |
| PolicyVersionActivated | Policy admin | All policy-driven domains | policy_version_id, effective_from | High | policy_version_id | Required | Projection retry | Block if conflict | Admin notice |
| PolicyVersionSuperseded | Policy admin | Domains, reporting | old_version, new_version | High | supersession_id | Required | Projection retry | Review conflict | Policy update |
| PolicyConflictDetected | Resolver | HR/legal reviewers | conflict_id, policy_ids, context | Restricted | conflict_id | Required | No | Controlled review | Conflict task |
| PolicyExceptionRequested | Operational domain | Policy reviewers | exception_id, rule_id, transaction | Restricted | exception_id | Required | No | Pending review | Reviewer task |
| PolicyExceptionApproved | Policy authority | Operational domain | exception_id, scope, expiry | Restricted | approval_id | Required | No | Manual correction | Result notice |
| PolicyExceptionDenied | Policy authority | Operational domain | exception_id, reason | Restricted | denial_id | Required | No | Close request | Result notice |
| RuleSetPublished | Policy Configuration | Rules/QS/Assessment engines | rule_set_id, version | High | rule_set_id | Required | Projection retry | Suspend use | Admin notice |
| RuleEvaluationCompleted | Rules Engine | Workflow/domain owner | evaluation_id, result summary | High | evaluation_id | Required | No duplicate | Manual review if error | Contextual |
| QualificationValidated | QS Engine | Recruitment/Career | validation_id, result | High | validation_id | Required | No duplicate | Pending review | Screening result |
| QualificationValidationRequiresReview | QS Engine | HR verifier | validation_id, missing data | High | validation_id | Required | No | Human verification | Review task |
| AssessmentFrameworkActivated | Policy Configuration | Recruitment/Career | framework_version_id | High | framework_version_id | Required | Projection retry | Block new cycles | Admin notice |
| RecommendationGenerated | Decision Support | Human reviewer | recommendation_id, use_case | Restricted | recommendation_id | Required | No duplicate | Mark failed/expired | Review task |
| RecommendationReviewed | Human reviewer | Workflow owner | recommendation_id, decision | Restricted | review_id | Required | No | Manual correction | Optional |
| RecommendationAccepted | Human reviewer | Audit/reporting | recommendation_id, action_ref | Restricted | review_id | Required | No | Manual correction | None |
| RecommendationRejected | Human reviewer | Audit/reporting | recommendation_id, reason | Restricted | review_id | Required | No | Manual correction | None |
| AIRequestBlocked | AI gateway | Security/governance | request_id, reason | Restricted | request_id | Required | No | Incident review if needed | Security alert |
| AIIncidentDetected | Monitoring/security | Governance | incident_id, severity | Restricted | incident_id | Required | No | Suspend model/use case | Security alert |
| AnalyticsRefreshCompleted | Reporting | Dashboards | refresh_id, counts | Internal | refresh_id | Required | Retry-safe | Mark stale if failed | None |
| AnalyticsRefreshFailed | Reporting | Admins | refresh_id, reason | Internal | refresh_id | Required | Retry | Mark stale | Admin alert |
| DataQualityIssueDetected | Reporting/Governance | Source domain owner | issue_id, severity, source | High | issue_id | Required | No | Correct source via domain | Data quality task |
| ComplianceRiskDetected | Analytics/Governance | Compliance owner | risk_id, metric, scope | High | risk_id | Required | No | Review risk | Compliance alert |

## Integration Rule

External AI, analytics, or policy retrieval services must use integration adapters. Notifications never become the source of business truth.
