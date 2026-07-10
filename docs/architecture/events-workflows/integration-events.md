# Integration Events

## Purpose

Define future external integration events and adapter boundaries.

| Integration | Direction | Event name | Payload summary | Authentication | Retries | Idempotency | Failure handling | Audit requirement | Sensitive-data restrictions |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Biometric devices | Inbound | AttendanceImportCompleted | import_batch_id, device_id, log_count, period. | Device/API credential. | Bounded retry. | import_batch_id + source hash. | Mark batch failed; allow manual replay. | Import log and actor/system. | Avoid storing raw biometric templates. |
| Payroll export | Outbound | PayrollExportGenerated | export_id, period_id, file_reference. | Authorized export user/API credential. | Manual-safe retry. | export_id. | Versioned regeneration. | Export log and access log. | No SMS/email attachment of payroll files. |
| Learning platform | Inbound/Outbound | LearningCompletionSynced | employee_id, program_id, completion_ref. | API token/OAuth. | Bounded retry. | external_reference. | Queue for manual reconciliation. | Sync log. | Minimal employee identifiers. |
| Email provider | Outbound | EmailDeliveryRequested | notification_delivery_id, template_id, recipient_ref. | Provider credential. | Retry with backoff. | notification_delivery_id. | Mark failed; workflow unaffected. | Delivery log. | Minimal sensitive content. |
| SMS provider | Outbound | SMSDeliveryRequested | notification_delivery_id, recipient_ref, short message. | Provider credential. | Retry with backoff. | notification_delivery_id. | Mark failed; workflow unaffected. | Delivery log. | No highly sensitive details. |
| Digital signature provider | Outbound/Inbound | DigitalSignatureRequested / DigitalSignatureCompleted | signature_request_id, document_ref, signer_ref. | Provider credential plus user authority. | Retry status checks. | signature_request_id. | Manual follow-up if expired/failed. | Signature request and result log. | Signer attribution required. |
| Government portals | Outbound/Inbound | EmployeeDataExportRequested / CSCActionReceived | export/submission refs and status. | Portal credential. | Controlled retry. | external_reference. | Manual reconciliation queue. | Submission/access log. | Send only approved payload. |
| Document archive | Outbound | ExternalDocumentArchived | document_id, archive_ref, checksum. | Storage credential. | Retry upload. | document_id + checksum. | Mark archive failed; preserve local ref. | Archive log. | No public links. |
| Mobile app | Outbound | MobilePushRequested | notification_delivery_id, user_id, template_id. | Push credential. | Retry with backoff. | notification_delivery_id. | Mark failed; in-app remains. | Delivery log. | Minimal content. |
| AI document processing | Outbound/Inbound | DocumentProcessingRequested / DocumentProcessingCompleted | document_ref, processing_type, result_ref. | Service credential. | Bounded retry. | processing_request_id. | Manual document review fallback. | Processing audit. | No unrestricted sensitive payloads. |

## Rule

Integration adapters must translate external data into domain commands or reviewed import records. External systems must not directly bypass domain validation or approval.
