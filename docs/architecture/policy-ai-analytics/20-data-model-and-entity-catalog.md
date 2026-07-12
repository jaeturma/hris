# 20 Data Model and Entity Catalog

## Purpose

Define conceptual entities for policy, rules, qualification, assessment, AI, and analytics. These are architecture entities only; do not create migrations during Phase 0.10.

## Entity Catalog

| Entity | Purpose | Owning domain | Key attributes | Relationships | Immutability | Classification | Audit | Retention |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Policy | Parent policy concept. | Policy Configuration | code, title, authority, type. | Has versions/sources. | Mutable metadata with audit. | High | Required | Policy schedule. |
| Policy Issuance | Specific order/memo/circular. | Policy Configuration | number, year, source document. | Source for policy versions. | Versioned. | High | Required | Permanent/reference if required. |
| Policy Version | Effective version. | Policy Configuration | version, dates, status, rules. | Links rules/workflows. | Immutable once used. | High | Required | Historical. |
| Policy Source | Source document/reference. | Policy Configuration/Documents | document_ref, URL, checksum. | Supports issuance. | Versioned. | High | Required | Reference schedule. |
| Policy Applicability | Applicability condition set. | Policy Configuration | scope, personnel, position, dates. | Used by resolver. | Versioned. | High | Required | Historical. |
| Policy Scope | Offices/groups covered. | Policy Configuration | office, position, personnel group. | Used by applicability. | Versioned. | High | Required | Historical. |
| Policy Relationship | Amendment/supersession relation. | Policy Configuration | relationship type, related policy. | Links policies. | Append-only. | High | Required | Historical. |
| Policy Supersession | Replacement record. | Policy Configuration | superseded, superseding, date. | Links versions. | Immutable. | High | Required | Historical. |
| Policy Amendment | Amendment record. | Policy Configuration | amended fields, basis. | Links versions. | Immutable. | High | Required | Historical. |
| Policy Approval | Human approval. | Policy Configuration | approver, capacity, date. | Activates version. | Immutable. | Restricted | Required | Historical. |
| Policy Activation | Activation event. | Policy Configuration | active_from, actor. | Enables use. | Immutable. | High | Required | Historical. |
| Policy Conflict | Conflict case. | Policy Configuration | type, affected policies, status. | Creates review task. | Append-only. | Restricted | Required | Historical. |
| Policy Resolution Snapshot | Chosen policy result. | Policy Configuration | inputs, selected versions, warnings. | Linked to transaction. | Immutable. | High | Required | Transaction retention. |
| Policy Exception | Approved/requested exception. | Policy Configuration | reason, basis, scope, expiry. | Links rule/transaction. | Immutable after decision. | Restricted | Required | Historical. |
| Policy Override | Technical/business override record. | Policy Configuration | authority, reason, affected rule. | Links transaction. | Immutable. | Restricted | Required | Historical. |
| Rule Definition | Rule identity. | Policy Configuration | code, name, category. | Has versions. | Versioned. | High | Required | Historical. |
| Rule Version | Executable rule version. | Policy Configuration | conditions, result, severity. | Source policy version. | Immutable once used. | High | Required | Historical. |
| Rule Condition | Condition expression. | Policy Configuration | input, operator, value. | Part of rule version. | Versioned. | High | Required | Historical. |
| Rule Action | Output/action of rule. | Policy Configuration | result, message, severity. | Rule version. | Versioned. | High | Required | Historical. |
| Rule Dependency | Rule ordering/dependency. | Policy Configuration | depends_on, priority. | Rule set. | Versioned. | High | Required | Historical. |
| Rule Set | Group of rules. | Policy Configuration | category, version, scope. | Used by engine. | Immutable once active. | High | Required | Historical. |
| Rule Evaluation | Evaluation run. | Operational owning domain | inputs, rule set, result. | Links transaction. | Immutable. | High | Required | Transaction retention. |
| Rule Evaluation Result | Individual result. | Operational owning domain | status, message, evidence. | Rule evaluation. | Immutable. | High | Required | Transaction retention. |
| Rule Test Case | Regression expectation. | Policy Configuration | inputs, expected result. | Rule version. | Versioned. | Internal | Required | Development history. |
| Qualification Standard Set | QS family. | Policy Configuration | position/group, source. | Has versions. | Versioned. | High | Required | Historical. |
| Qualification Standard Version | Effective QS. | Policy Configuration | education, training, experience, eligibility. | Used by QS engine. | Immutable once used. | High | Required | Historical. |
| Qualification Requirement | Single requirement. | Policy Configuration | category, minimum/preferred. | QS version. | Versioned. | High | Required | Historical. |
| Qualification Requirement Group | Grouping logic. | Policy Configuration | all/any/optional. | Requirements. | Versioned. | High | Required | Historical. |
| Qualification Equivalency | Equivalent evidence rule. | Policy Configuration | source, target, conditions. | QS version. | Versioned. | High | Required | Historical. |
| Qualification Substitution | Substitution rule. | Policy Configuration | substitute, basis. | QS version. | Versioned. | High | Required | Historical. |
| Qualification Validation | Validation run. | Recruitment/Career | applicant/employee, QS version, result. | Links evidence. | Immutable. | High | Required | Transaction retention. |
| Qualification Snapshot | Frozen validation context. | Recruitment/Career | inputs, evidence versions. | Transaction. | Immutable. | Restricted | Required | Transaction retention. |
| Assessment Framework | Framework family. | Policy Configuration | name, pathway. | Has versions. | Versioned. | High | Required | Historical. |
| Assessment Framework Version | Effective framework. | Policy Configuration | criteria, scoring, aggregation. | Workflow cycles. | Immutable once used. | High | Required | Historical. |
| Assessment Criterion | Score category. | Policy Configuration | name, max points, rule. | Framework version. | Versioned. | High | Required | Historical. |
| Assessment Subcriterion | Detailed score item. | Policy Configuration | name, scale, evidence. | Criterion. | Versioned. | High | Required | Historical. |
| Scoring Scale | Score options. | Policy Configuration | scale, values, labels. | Criterion. | Versioned. | High | Required | Historical. |
| Evidence Requirement | Required proof. | Policy Configuration | doc type, verification. | Framework/QS. | Versioned. | High | Required | Historical. |
| Aggregation Rule | Score aggregation. | Policy Configuration | method, rounding, weights. | Framework. | Versioned. | High | Required | Historical. |
| Tie-Breaking Rule | Ranking tie rule. | Policy Configuration | order, conditions. | Framework. | Versioned. | High | Required | Historical. |
| Evaluator Role | Required evaluator type. | Policy Configuration | role, assignment rule. | Framework. | Versioned. | High | Required | Historical. |
| Evaluation Snapshot | Frozen evaluation. | Recruitment/Career | scores, evidence, framework. | Transaction. | Immutable. | Restricted | Required | Transaction retention. |
| Ranking Configuration | Ranking rule set. | Policy Configuration | sort, gates, outputs. | Framework. | Immutable once used. | High | Required | Historical. |
| AI Use Case | Approved AI purpose. | Governance/AI | name, risk, owner. | Model/prompt. | Versioned. | High | Required | Active plus history. |
| AI Model | Model family. | Governance/AI | provider, type, deployment. | Versions. | Versioned. | Restricted | Required | Lifecycle. |
| AI Model Version | Deployed model. | Governance/AI | version, approval, limits. | Requests. | Immutable once used. | Restricted | Required | Reproducibility. |
| AI Provider | Provider record. | Integration/Governance | contract, location, controls. | Models. | Versioned. | Restricted | Required | Vendor retention. |
| AI Risk Assessment | Risk review. | Governance/AI | risks, mitigations, approval. | Use case. | Immutable after approval. | Restricted | Required | Governance retention. |
| AI Approval | Deployment approval. | Governance/AI | approver, scope, expiry. | Use case/model. | Immutable. | Restricted | Required | Historical. |
| AI Prompt Template | Prompt family. | Governance/AI | name, purpose. | Versions. | Versioned. | High | Required | Historical. |
| AI Prompt Version | Effective prompt. | Governance/AI | instructions, tools, limits. | Requests. | Immutable once used. | Restricted | Required | Reproducibility. |
| AI Knowledge Source | Approved source. | Policy/AI | source, status, version. | Retrieval. | Versioned. | High | Required | Source retention. |
| AI Request | User request. | Governance/AI | user, context, inputs, scope. | Response. | Immutable. | Restricted | Required | Reproducibility. |
| AI Response | Output. | Governance/AI | content, sources, warnings. | Review. | Immutable. | Restricted | Required | Reproducibility. |
| AI Recommendation | Advisory result. | Decision Support | state, confidence, explanation. | Human review. | Versioned. | Restricted | Required | Transaction retention. |
| AI Explanation | Explainability record. | Decision Support | data used, rules, limits. | Recommendation. | Immutable. | Restricted | Required | Reproducibility. |
| AI Human Review | Reviewer decision. | Decision Support | accepted/rejected, reason. | Recommendation. | Immutable. | Restricted | Required | Historical. |
| AI Incident | AI issue/security event. | Governance/AI | severity, impact, action. | Use case/model. | Append-only. | Restricted | Required | Incident retention. |
| AI Monitoring Metric | Monitoring result. | Governance/AI | metric, value, date. | Model/use case. | Append-only. | High | Required | Lifecycle. |
| Metric Definition | Metric identity. | Reporting | name, formula, owner. | Versions. | Versioned. | High | Required | Historical. |
| Metric Version | Effective metric. | Reporting | formula, filters, scope. | Dashboards. | Immutable once used. | High | Required | Historical. |
| KPI Definition | KPI target. | Reporting | target, threshold, owner. | Dashboards. | Versioned. | High | Required | Historical. |
| Dashboard Definition | Dashboard family. | Reporting | audience, widgets. | Versions. | Versioned. | High | Required | Historical. |
| Dashboard Version | Effective dashboard. | Reporting | layout, metrics, filters. | Access logs. | Immutable once snapshotted. | High | Required | Historical. |
| Report Definition | Report family. | Reporting | query, filters, outputs. | Snapshots. | Versioned. | High | Required | Historical. |
| Report Snapshot | Generated report. | Reporting | filters, source date, output. | Exports. | Immutable. | Restricted | Required | Report retention. |
| Data Mart | Read model. | Reporting | sources, refresh policy. | Analytics. | Rebuildable. | High | Required | Operational. |
| Data Refresh | Refresh run. | Reporting | date, status, counts. | Data mart. | Append-only. | Internal | Required | Operational. |
| Data Quality Result | Quality finding. | Reporting/Governance | rule, result, severity. | Source domain. | Append-only. | High | Required | Governance retention. |
| Analytics Access Log | Dashboard/report access. | Reporting | user, scope, export. | Audit. | Immutable. | Restricted | Required | Audit retention. |
