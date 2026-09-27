# Architecture and delivery decision log

The requirements should determine the architecture. Use this file to compare alternatives without committing to a product before the operating model is approved.

## Capability map to size

| Capability | Minimum decision |
| --- | --- |
| Customer context | Source of truth, permitted view, identity/authority and safe contact |
| Interaction capture | Channel events, original receipt and attachments |
| Case management | State, issue model, ownership, tasks and linked workflows |
| Policy/rules | Versioned classification, clocks, exceptions and approvals |
| Communications | Templates, accessibility, dispatch and evidence |
| Remedy execution | Approval, authoritative posting, reconciliation and failure handling |
| Knowledge | Approved policy content, version, effective date and search |
| Reporting | Operational, conduct, IDR submission and audit export |
| Security/privacy | Role/attribute access, audit, retention, incidents and data boundaries |
| Integration | Customer, banking, card, fraud, hardship, telephony, document and AFCA |
| Operations | Monitoring, support, recovery, manual fallback and change control |

## Build / configure / buy evaluation

Score each option against the same approved requirements. Include three-year and five-year cost, implementation time, migration risk, product fit, regulatory change effort, user experience, data portability, security and privacy responsibilities, service-provider risk, operability and exit cost. Document any mandatory capability that a proposed option cannot meet.

## Architecture decision record template

- ADR ID and title:
- Date, status and decision owner:
- Business requirement IDs:
- Context and constraints:
- Options considered:
- Evidence and evaluation criteria:
- Decision and why:
- Consequences, trade-offs and risks:
- Revisit trigger/date:
- Approvals:

## Initial decisions required

| ID | Decision | Reason it matters | Owner |
| --- | --- | --- | --- |
| ADR-001 | System of record for customer, case, documents, communications and monetary remedy | Prevents conflicting truth and ambiguous reconciliation | Data and architecture |
| ADR-002 | Modular case/issue model and workflow engine boundary | Controls complexity when products have different rules | Product and architecture |
| ADR-003 | Versioned policy and deadline service | Makes regulatory and policy change testable | Compliance and architecture |
| ADR-004 | Integration pattern for core banking and card systems | Determines real-time behaviour, failure modes and security | Architecture and core-system owners |
| ADR-005 | Data storage, residency, encryption and retention | Determines privacy and operational controls | Privacy and security |
| ADR-006 | Availability and manual fallback | Protects receipt and deadlines during outages | Operations and architecture |
| ADR-007 | AI services and permitted actions | Determines data-sharing, human review and monitoring | Product, privacy and risk |
| ADR-008 | Platform choice and vendor exit | Determines lifetime cost and portability | Sponsor and architecture |

## Suggested implementation slices

1. Establish customer/representative lookup, intake, immutable receipt and manual fallback.
2. Add complaint triage, linked workflows, ownership, versioned deadlines and alerts.
3. Add investigation, evidence, response drafting/approval and safe dispatch.
4. Add remedy execution and reconciliation, closure rules and audit export.
5. Add systemic issue linkage, analytics, regulatory reporting and AFCA pack.
6. Add further channels and carefully evaluated automation.

Each slice needs policy approval, acceptance scenarios, security/privacy review, integration contract, support runbook and traceable evidence before release.
