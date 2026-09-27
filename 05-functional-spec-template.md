# Functional and control specification template

Create one section per capability or epic after the BRD is approved. The system design may change, but observable behaviour and tests must trace to the business requirement.

## 1. Identification

- Feature ID and name:
- BRD requirement IDs:
- Product owner and operational owner:
- Status and version:
- In-scope legal entity, customer, product and channel:
- Policy/rule version:

## 2. Actors, permissions and data

| Actor | May view | May create/change | May approve | Restrictions |
| --- | --- | --- | --- | --- |
| Customer |  |  |  |  |
| Frontline agent |  |  |  |  |
| Specialist |  |  |  |  |
| Team lead |  |  |  |  |
| Audit/compliance |  |  |  |  |
| Service account |  |  |  |  |

For each field, record: name; definition; type/format; allowed values; required-at-stage; source of truth; sensitivity; validation; retention; API/reporting mapping; change history.

## 3. Trigger and preconditions

- Triggering event and authoritative timestamp:
- Preconditions:
- Identity/authority level required:
- Applicable business rule selection:
- Idempotency key or duplicate behaviour:

## 4. Normal flow

| Step | Actor/system | Action | Validation | State change | Audit event | Customer-visible effect |
| --- | --- | --- | --- | --- | --- | --- |
| 1 |  |  |  |  |  |  |

## 5. Alternate and failure flows

Cover invalid or partial input; wrong customer; duplicate; unavailable dependency; timeout; retry; stale/conflicting data; wrong owner; missing approval; unsafe contact; communication failure; deadline risk; withdrawal; reopen; reversal and manual fallback.

| Scenario | Detection | System behaviour | Human owner | Customer effect | Recovery / reconciliation |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

## 6. State and time rules

- State diagram or transition table:
- Clock start event, timezone and calendar:
- Applicable maximum and internal targets:
- Warning thresholds and escalation:
- Valid delay or exception criteria:
- Rule changes for open cases:
- Test examples with expected dates:

## 7. Integrations and messages

| System | Direction/event | Payload and classification | Contract/version | Retry and idempotency | Failure owner | Reconciliation |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |

## 8. Communications and documents

- Template ID/version, language and accessible formats:
- Mandatory content and conditional clauses:
- Approval and dispatch method:
- Recipient verification and safe-contact check:
- Delivery evidence, bounce and re-send handling:

## 9. Controls and operational requirements

- Access rules, segregation of duties and break-glass:
- Privacy purpose, minimisation, masking and retention:
- Audit events and monitoring alerts:
- Performance, availability and recovery target:
- Manual workaround and back-entry:
- Support runbook and configuration owner:

## 10. Acceptance tests

| Test ID | Given | When | Then | Source requirement | Evidence |
| --- | --- | --- | --- | --- | --- |
| AT-001 |  |  |  |  |  |

Test normal, boundary, exception, security, accessibility and integration behaviour. Use synthetic data and include a trace to each approved rule.

## 11. Decisions and approval

- Open decisions:
- Risks and mitigations:
- Product, process, compliance, privacy/security, architecture and test approvals:
