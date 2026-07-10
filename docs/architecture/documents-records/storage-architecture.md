# Storage Architecture

## Purpose

Define storage layers, privacy, backup, and disaster-recovery expectations.

## Recommended Storage Layers

Private local storage for development, private object storage for production, encrypted backup storage, archive storage, temporary-processing storage, quarantine storage, virus-scan staging, and OCR-processing staging.

## Storage Rules

- Do not store sensitive documents in `public/`.
- Store generated filenames and safe storage references.
- Logical paths should support office, domain, document type, and retention classification without exposing sensitive names.
- Private access must be enforced through the application.
- Signed temporary URLs must be short-lived and generated only after authorization.
- Use encryption at rest and in transit where supported.
- Backup, replication, lifecycle policy, retention lock, disaster recovery, and storage monitoring must be planned before production.

## Storage Separation

Document metadata belongs to the HRIS database. Binary object storage stores files. Archive storage may store long-term official copies. Temporary and quarantine storage must never be treated as official record storage.
