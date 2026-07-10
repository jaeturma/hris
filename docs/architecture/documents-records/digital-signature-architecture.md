# Digital Signature Architecture

## Purpose

Define readiness for PNPKI, authorized digital certificates, external signature providers, internal approval signatures, detached signatures, embedded PDF signatures, multiple signatories, and signature validation.

## Signature Distinctions

| Type | Meaning | System Treatment |
| --- | --- | --- |
| Approval action | Workflow decision by authorized user. | Structured approval record, not automatically a signed document. |
| Electronic acknowledgement | User confirms receipt or agreement. | Audit record with actor and timestamp. |
| Image of signature | Scanned or pasted signature image. | Visual mark only; not certificate-based digital signature. |
| Electronic signature | Electronic indication of signing intent. | Requires policy/legal validation before official use. |
| Certificate-based digital signature | Signature using authorized certificate infrastructure. | Store signature and validation metadata. |

## Signature Metadata

Signer, signer authority, delegated or acting capacity, certificate reference, certificate validity, certificate revocation status where available, timestamp authority, signature reason, signature location, signed document hash, provider reference, validation result, validation time, and archive reference.

## Rules

- Digital signing must require authorized human action.
- The system must not sign documents automatically on behalf of an official.
- Signed files must become immutable.
- Signature validation results must be stored.
- Expired certificates must not automatically invalidate a signature valid when properly timestamped, subject to applicable validation rules.
- Digital-signature failure must not silently finalize the workflow.
- Signature delegation must be explicit and auditable.
- Multiple and sequential signatories must preserve order, signer role, and timestamp.
