# Integration Domain

## Purpose

Own adapters and integration boundaries for external systems without embedding core HR business logic.

## Business Scope

Biometric Adapter, Email, SMS, Digital Signature, Document Storage, Payroll Export, Learning Platform Integration, Government Portal Integration, API Clients, Import Jobs.

## Out of Scope

Core HR decisions, attendance rules, payroll preparation rules, document verification, and policy interpretation.

## Main Entities

Integration Adapter, API Client, Import Job, Export Job, Sync Log, External Reference, Webhook Event.

## Aggregate or Ownership Candidates

Integration configuration, import job, export job, sync log.

## Key Business Rules

- Adapters translate external data into application commands or events.
- External systems must not directly write operational records.
- Failed imports and exports require retry and audit history.

## Commands or Use Cases

Import biometric logs, send email, send SMS, request digital signature, export payroll file, sync learning completion.

## Domain Events

ExternalImportReceived, IntegrationExportGenerated, IntegrationFailed, DigitalSignatureRequested, MessageSent.

## Dependencies

Depends on Core Platform, Policy and Configuration, and the target operational domain for commands. Operates at the system boundary.

## Policy Dependencies

Data Privacy Act, ICT security rules, records management, external system agreements, government portal requirements.

## Security Sensitivity

Restricted.

## Audit Requirements

Log external requests, imports, exports, failures, retries, credentials changes, and data transfer metadata.

## Reports Produced

Integration status report, import log, export log, failed sync report, external reference report.

## Implementation Phase

Later phases, except basic email/document storage references as needed.
