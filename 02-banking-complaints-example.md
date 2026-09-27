# Worked example: Australian bank complaints capability

**Example only.** Assumed organisation: a retail bank with deposits, cards and home loans, phone/branch/web/email intake, a central complaints team and AFCA membership. Policy, product, licence, Banking Code subscription and applicable rules need owner approval. IDs below illustrate how to turn interviews into buildable requirements.

## 1. Example business outcomes

| ID | Outcome | Baseline to collect | Proposed measure |
| --- | --- | --- | --- |
| BO-01 | No qualifying complaint is lost between frontline and specialist teams | Sample contact review and case reconciliation | All sampled qualifying contacts have linked case and original receipt timestamp |
| BO-02 | Customers receive timely, understandable responses | Current age and quality review | Compliance with applicable IDR maximum; separate internal target and response-quality score |
| BO-03 | Agreed remedies actually occur | Case-to-ledger reconciliation | No case marked complete with an unexecuted required remedy |
| BO-04 | Repeated harm is found and fixed | Current root-cause and incident records | Suspected systemic signals reviewed, escalated and tracked to decision |
| BO-05 | Customer information is used safely | Access review and privacy incidents | Role-based access, monitored sensitive views and tested retention controls |

## 2. Service taxonomy

| Contact type | Example | Primary workflow | Complaint link |
| --- | --- | --- | --- |
| Enquiry | "What is this fee?" | Answer or research | Create complaint if dissatisfaction with product/service or handling is expressed |
| Service request | "Please change my mailing address" | Authenticate, action, confirm | Link complaint if request handling itself generates dissatisfaction |
| Transaction dispute | "I did not authorise this card payment" | Card/fraud investigation and protective actions | A report alone is not necessarily an IDR complaint under RG 271.33; dissatisfaction with the outcome or handling can be |
| Hardship request | "I cannot meet this month's mortgage payment" | Credit hardship assessment | A request alone is not necessarily an IDR complaint; separate dissatisfaction can be |
| Complaint | "You charged me the fee again and nobody fixed it" | IDR process | Record from first qualifying expression, even if a frontline agent resolves it |
| External dispute | "I have gone to AFCA" | AFCA workflow | Link to original complaint, preserve external reference and deadlines |
| Systemic issue | "This fee defect affects many accounts" | Conduct/root-cause and remediation workflow | Link individual cases and affected cohort, do not replace them |

Source: [ASIC RG 271, especially 271.27–.35](https://download.asic.gov.au/media/3olo5aq5/rg271-published-2-september-2021.pdf).

## 3. Example end-to-end journey

1. **Receive.** Capture original expression, channel, receipt time and legal entity. Permit low-friction intake before full identity is established. Initiate urgent protective action where needed.
2. **Recognise and classify.** Agent identifies complaint and any parallel service, fraud, card or hardship process. Link records without merging clocks.
3. **Acknowledge.** Record acknowledgement method, time, recipient and any safe-contact or accessibility need.
4. **Triage.** Assess product, issue, immediate harm, vulnerability, urgency, applicable rule version, due date, ownership and conflict of interest.
5. **Investigate.** Gather account and transaction history, policy, correspondence and customer evidence. Record material facts, gaps and conclusions.
6. **Decide.** Resolve each issue, select remedy and obtain approvals. Prepare reasons for any rejection or partial rejection.
7. **Respond.** Issue the required response or document a valid short-resolution exception. If an allowed delay applies, send an approved delay notice before the due date.
8. **Execute outcome.** Post refund/compensation or corrective action in the authoritative system. Reconcile and retain evidence.
9. **Close and learn.** Close under the approved policy, record category/root cause/outcome, and review for repeated harm.
10. **Escalate externally if needed.** Link AFCA case, evidence requests, decision and implementation. Preserve the customer's right to access AFCA.

### Proposed case states

Received → Triage → Investigation → Decision pending → Response pending → Outcome implementation → Closed. Alternate states: awaiting information, escalation review, AFCA active, withdrawn. These are **workflow states**, not automatic pauses to any regulatory clock. Each transition requires an actor, timestamp, reason and validation.

## 4. Example business rules for compliance review

| Rule ID | Candidate rule | Source / question to validate |
| --- | --- | --- |
| BR-01 | A qualifying expression of dissatisfaction creates a complaint record with the original receipt time; internal transfer does not restart the clock. | [RG 271.27–.35, .106](https://download.asic.gov.au/media/3olo5aq5/rg271-published-2-september-2021.pdf) |
| BR-02 | Track prompt acknowledgement; ASIC expects within 24 hours or one business day, or as soon as practicable. | RG 271.51–.52; define local implementation target and exception reason. |
| BR-03 | Select the deadline by complaint type and rule version. Standard IDR response maximum is 30 calendar days; specified credit/default/hardship complaints can use 21-calendar-day processes. | RG 271.56–.60, Table 2; legal owner to map precise product scenarios. |
| BR-04 | A written IDR response states final outcome, AFCA right and contact details; partial/full rejection includes reasons and supporting findings. | RG 271.53–.55. |
| BR-05 | The five-business-day written-response exception only applies when conditions are met. Provide written response if requested or when a listed exception such as hardship applies. | RG 271.71–.75. |
| BR-06 | A delay notice is available only for specified complexity or beyond-control reasons and must be sent before the original maximum expires with reason and AFCA details. | RG 271.64–.66. |
| BR-07 | Record complaint outcome, remedy and compensation; verify agreed remedy implementation before operational completion. | RG 271.164–.165. |
| BR-08 | Analyse complaint data for possible systemic issues, escalate promptly and link confirmed issues to remediation. | RG 271.118–.121; [RG 277](https://www.asic.gov.au/regulatory-resources/find-a-document/regulatory-guides/rg-277-consumer-remediation). |
| BR-09 | Capture all qualifying complaints for IDR reporting, including those resolved quickly; maintain a versioned reporting mapping. | [ASIC IDR reporting page](https://www.asic.gov.au/regulatory-resources/financial-services/dispute-resolution/internal-dispute-resolution-data-reporting); confirm current handbook. |
| BR-10 | Only authorised staff can view sensitive case material; collection, use, retention and disclosure follow approved privacy purposes. | [OAIC APPs](https://www.oaic.gov.au/privacy/australian-privacy-principles/read-the-australian-privacy-principles), [APP 11](https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-guidelines/chapter-11-app-11-security-of-personal-information). |

**Important clock example:** a complaint received Sunday evening has Sunday as the receipt date. RG 271 explains that the count starts with the next calendar or business day as relevant. Business-day calculation, holidays and special credit exceptions require a tested rule table; changing queue or owner cannot change receipt.

## 5. Example functional requirements

| ID | Requirement | Acceptance evidence |
| --- | --- | --- |
| FR-001 | Agent can create a complaint from any in-scope channel and preserve original words, channel and receipt timestamp. | Phone, branch, web and email examples all produce searchable cases; timestamp correction creates an audit event. |
| FR-002 | Agent can link a complaint to a service request, card dispute or hardship case without combining statuses or clocks. | Linked cases show distinct type, owner, due date and history. |
| FR-003 | Triage shows the selected rule, source version, calculated due date and internal warning dates. | Date cases cover weekend, public holiday, leap year and daylight-saving boundary. |
| FR-004 | Work queues route by product, skill, priority and conflict rules with fallback owner. | Unassigned case triggers exception alert; transfer preserves original receipt. |
| FR-005 | The system records acknowledgement, progress messages, evidence requests, final response and delivery failures. | Each message has version, author, approver if needed, recipient, channel and send result. |
| FR-006 | Investigator can record issues, evidence, findings, missing facts, decision and reviewer separately. | Rejection response can cite each issue and supporting material; hidden material stays restricted. |
| FR-007 | Response generator requires final outcome, AFCA details and reasons for rejected issues. | Missing required fields prevent dispatch; human reviewer can edit before send. |
| FR-008 | Remedy task links the case to core banking/ledger execution and reconciliation. | Case reports outstanding remedy until authoritative confirmation arrives. |
| FR-009 | Agent can link cases to a suspected systemic issue and escalate to the designated owner. | Trend alert and manual escalation both create review work with outcome record. |
| FR-010 | Reporting export is reconcilable to case population and preserves reporting schema version. | Counts and exceptions reconcile for a sample period. |
| FR-011 | Privacy controls mask restricted material and log access, export and override. | Role matrix tests include family violence and staff-misconduct scenarios. |
| FR-012 | Outage intake form or procedure preserves original receipt time and can be reconciled on re-entry. | Simulated outage shows no lost or duplicate complaint. |

## 6. Example nonfunctional requirements to quantify

| ID | Requirement to finalise | Measurement method |
| --- | --- | --- |
| NFR-001 | Availability and recovery targets per critical journey | Business impact analysis and disaster-recovery exercise |
| NFR-002 | Search and case-open performance at defined concurrent load | Load test with production-like synthetic case volumes |
| NFR-003 | Retention and deletion/de-identification by record category | Policy mapping and scheduled-job evidence |
| NFR-004 | Least-privilege access and tamper-evident audit | Role test, access review and audit-log integrity test |
| NFR-005 | Accessible agent and customer journeys | Assistive-technology tests with representative users |
| NFR-006 | Data export, reconciliation and backup restore | Report-to-source reconciliation and restore exercise |

Do not fill these with arbitrary percentages or response times. Have the business and risk owners set measurable targets.

## 7. Example acceptance scenarios

1. **Resolved quickly:** a customer complains by phone about a duplicate fee; agent refunds it within the call. The case is still recorded and classified. The system evaluates whether a written response is required and records why.
2. **Requested written response:** same facts, customer requests a written decision. The short-resolution exception must not suppress the written response.
3. **Credit hardship plus complaint:** customer requests hardship help and separately complains about staff conduct. Create linked workflows; select applicable rules for each and protect sensitive notes.
4. **Incorrect owner:** a branch receives a complaint for the card team. Transfer it; original receipt and response deadline remain visible and unchanged.
5. **Partial rejection:** two issues, one upheld and one rejected. Final response addresses both and includes findings, reasons, AFCA right and contact details.
6. **Remedy failed:** approved refund fails in the ledger. The case remains visible on an outcome-exception worklist until corrected and reconciled.
7. **Potential systemic issue:** ten similar fees appear across products. Create an investigation with cohort estimate, accountable owner, decision, actions and links to individual complaints.
8. **Unsafe contact:** customer reports family violence and a shared postal address. Prevent standard correspondence until safe-contact instructions are reviewed.
9. **Delay:** a complex case qualifies for a permissible delay. Approved notification is sent before the applicable maximum expires; customer still receives AFCA details.
10. **Outage:** web form and CRM are unavailable. Manual record is later entered with true receipt time, duplicate check and full audit trail.

## 8. Ownership map to validate

| Decision/action | Proposed accountable owner |
| --- | --- |
| Definition, taxonomy and IDR policy | Complaints policy owner with compliance |
| Case triage and investigation | Complaints operations |
| Legal interpretation and response exceptions | Legal/compliance |
| Safe contact and vulnerable-customer handling | Customer support policy and privacy |
| Financial remedy approval and execution | Product owner plus finance/core operations |
| Systemic investigation and remediation | Conduct risk/remediation owner |
| Security and privacy controls | Security and privacy officers |
| Reporting submission | Regulatory reporting owner |
| Architecture, integration and recovery | Technology owner |

## 9. Open decisions before build

- Which legal entities and product lines are covered?
- Does the bank subscribe to the 2025 Banking Code, and which clauses apply?
- What exact rule table applies to each credit and card scenario?
- Which system is authoritative for customer identity, payments and documents?
- What sensitive-data categories and safe-contact controls are mandatory?
- What retention periods and legal-hold rules apply to each artefact?
- What are the bank-approved availability, recovery, performance and accessibility targets?
- Which automated actions, if any, may occur without human review?
