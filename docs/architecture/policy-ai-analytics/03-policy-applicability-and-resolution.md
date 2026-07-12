# 03 Policy Applicability and Resolution

## Purpose

Define how the system determines applicable policies for a transaction and handles conflicts without guessing silently.

## Policy Hierarchy and Precedence

```mermaid
flowchart TD
    A[Philippine laws and national regulations] --> B[CSC issuances and ORAOHRA]
    B --> C[National DepEd Orders and Memoranda]
    C --> D[Approved DepEd Central Office policies]
    D --> E[Regional Memoranda]
    E --> F[Division Memoranda]
    F --> G[Local office procedures]
    G --> H[System defaults]
```

Local policies may implement or clarify but must not override higher-level mandatory requirements. System defaults apply only when no policy-controlled rule is required.

## Applicability Inputs

Transaction date, application date, publication date, vacancy type, personnel category, position, position group, salary grade, job family, office type, Region, Division, District, School, Implementing Unit status, appointment type, promotion type, career-progression pathway, reclassification pathway, funding source, plantilla type, applicant status, employee status, special program, policy exception, and temporary authority.

## Resolution Flow

```mermaid
flowchart TD
    A[Transaction context] --> B[Find active policy versions by date and scope]
    B --> C[Apply hierarchy and applicability filters]
    C --> D{Single clear policy set?}
    D -- Yes --> E[Create policy resolution snapshot]
    D -- No --> F[Detect conflict or missing rule]
    F --> G[Create controlled policy review task]
    G --> H[Authorized HR/legal resolution]
    H --> E
```

## Conflict Scenarios

Two active policies cover the same transaction, local policy conflicts with national policy, policy becomes effective during active workflow, transition provisions are unclear, policy is uploaded but unverified, structured rules are missing, retroactive effect is claimed, directive suspends a rule, temporary exemption exists, or emergency procedure applies.

## Policy Conflict and Escalation Flow

```mermaid
flowchart TD
    A[Resolver detects conflict] --> B[Block automatic policy selection]
    B --> C[Create policy conflict case]
    C --> D[Notify authorized HR/legal policy reviewer]
    D --> E{Reviewer resolves?}
    E -- Needs source --> F[Request source verification or clarification]
    E -- Resolved --> G[Record resolution, basis, and scope]
    F --> D
    G --> H[Create resolution snapshot]
    H --> I[Resume, suspend, migrate, or restart workflow per authorized decision]
```

## Resolution Snapshot

Every official transaction must preserve selected policy versions, rejected alternatives, applicability inputs, resolver version, timestamp, user/system actor, office context, and warnings.
