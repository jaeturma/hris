# Document Security

## Purpose

Define file validation, malware controls, preview/download safety, and exfiltration protections.

## Required Controls

MIME validation, extension validation, file-signature validation, upload-size limits, malware scanning, password-protected file handling, macro-enabled file restrictions, executable-file blocking, image metadata handling, PDF sanitization, document preview isolation, download authorization, temporary URL expiration, watermarking where appropriate, exfiltration monitoring, bulk-download restrictions, and rate limiting.

## Rules

- Do not trust client-provided MIME type or extension alone.
- Quarantine files until required security checks complete.
- Block executable and unsafe macro-enabled files unless a verified business process requires special handling.
- Preview services must not expose original storage paths.
- Bulk downloads must require explicit permission and audit logging.
- Sensitive file previews and downloads should be watermarked where appropriate.
- Failed security checks must route to safe failure states.
