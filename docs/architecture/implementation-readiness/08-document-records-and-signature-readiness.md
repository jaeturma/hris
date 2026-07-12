# Document, Records, and Signature Readiness

## Readiness matrix

| Area | Architecture position | Remaining approval | Rating |
|---|---|---|---|
| Private storage/metadata | originals private; metadata relational | storage platform, malware scanning, limits | Amber |
| Access/audit | independent authorization and access log | classification-to-role matrix, log retention | Amber |
| Versioning/verification | preserve original and replacement/verification history | verifier authority and correction process | Amber |
| Generated/final records | template versions; finalized immutable | approved templates/signatories | Amber by module |
| Retention/disposition/holds | lifecycle defined | official schedule and records authority | Red |
| Digital signature | certificate-based trust; scanned image not equivalent | PNPKI/legal trust, timestamp/revocation/validation/archive | Red |
| OCR/AI extraction | raw extraction distinct; human verification | privacy/vendor/accuracy controls | Red / deferred |

## Records rules

- A binary document never substitutes for an employee, appointment, service-record or decision row.
- Preserve original bytes, checksum, source, classification, ownership, version, access history and verification outcome.
- Finalized or signed records are immutable; correction creates a linked successor or authorized annotation.
- Legal/audit hold overrides disposition. Destruction requires approved authority and evidence.
- A signature image is not a certificate-based digital signature.

## Relationship sequence

Upload → validate type/size → malware-scan integration point → preserve original → classify/authorize → record metadata/checksum → verify evidence → link to structured record → version/finalize → retain/hold/dispose under approved schedule.

**Assessment: Red for document-system implementation, Gray for Phase 1 except policy-source metadata planning.** C-09 records schedules and C-10 signature trust block their affected modules, not WP-1 baseline work.

