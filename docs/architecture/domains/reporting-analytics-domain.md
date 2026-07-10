# Reporting and Analytics Domain

## Purpose

Own cross-domain reports, dashboards, analytics, exports, report snapshots, and management views.

## Business Scope

Operational Reports, Management Dashboards, Compliance Reports, Workforce Analytics, Promotion Readiness Analytics, Vacancy Analytics, PRIME-HRM Readiness Analytics, Export Jobs, Report Snapshots.

## Out of Scope

Operational write rules, policy interpretation, source record correction, and workflow approvals.

## Main Entities

Report Definition, Dashboard, Export Job, Report Snapshot, Analytics View, Report Filter, Scheduled Report.

## Aggregate or Ownership Candidates

Report definition, export job, report snapshot.

## Key Business Rules

- Reporting may read across domains but must not own operational business rules.
- Sensitive report exports require permission, office scope, and audit.
- Report snapshots must preserve the source date, filter, policy context, and actor.

## Commands or Use Cases

Generate report, schedule export, create dashboard snapshot, run analytics query, export report.

## Domain Events

ReportGenerated, ExportJobQueued, ReportSnapshotCreated, DashboardViewed.

## Dependencies

Reads from all domains. Depends on Core Platform for permissions and Organization for scope.

## Policy Dependencies

PRIME-HRM reporting, DepEd reporting requirements, Data Privacy Act, records management.

## Security Sensitivity

High.

## Audit Requirements

Log report generation, dashboard access, export jobs, sensitive filters, and downloaded files.

## Reports Produced

All operational, management, compliance, analytics, and export reports.

## Implementation Phase

Phase 10, with basic operational reports emerging per module.
