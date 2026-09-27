# Discovery question bank

Use these questions in interviews and process walkthroughs. For every answer, ask for a recent real example, the policy or data that supports it, the exception, the accountable owner and the decision needed. Record **current state** and **target state** separately. Question IDs stay stable so answers can be linked to requirements and tests.

## A. Strategy, boundaries and value

- **STR-01** What business problem justifies a new CRM: customer harm, compliance, handling time, cost, fragmented data, product strategy or something else? What evidence quantifies it?
- **STR-02** Which outcomes matter most to customers, staff, management and regulators? How will success be measured and what is today's baseline?
- **STR-03** Is the system for one legal entity, a group, a shared service or an external product sold to other firms? Who is the controller of each record?
- **STR-04** Which customer segments, brands, products, countries, languages and channels are in the first release and later releases?
- **STR-05** Are enquiries, service requests, complaints, disputes, fraud reports, hardship requests and remediation cases all in scope? Which are separate workflows that can be linked?
- **STR-06** Which existing capabilities will remain system of record for customers, accounts, transactions, documents, payments, identity and communications?
- **STR-07** What work must remain possible if the CRM is unavailable? Which operations are critical?
- **STR-08** What are the budget, delivery date, staffing, implementation constraints, procurement rules and time horizon for total cost of ownership?
- **STR-09** What would make buying, configuring, composing or building the system preferable? Which capabilities are genuinely differentiating?
- **STR-10** Who can approve scope, policy interpretation, changes, risk acceptance and go-live?

## B. People, customer segments and relationships

- **CUS-01** Who may contact the organisation: customer, prospective customer, former customer, joint account holder, guarantor, executor, adviser, advocate, attorney, carer or regulator?
- **CUS-02** What proof establishes the right of each person to make an enquiry, lodge a complaint, see information or accept a remedy?
- **CUS-03** How are personal customers, small businesses, trusts and corporate customers represented? How are multiple roles linked to one person?
- **CUS-04** What is the authoritative customer identifier? What happens if no customer record exists or identity is uncertain?
- **CUS-05** How are duplicate, merged, split, deceased, dormant or fraud-flagged customer records handled?
- **CUS-06** Which relationship and account details are necessary for staff to resolve a case? Which should be hidden by default?
- **CUS-07** How is a customer's preferred name, pronouns, language, channel, contact time or accessible format recorded and honoured?
- **CUS-08** How are vulnerability and support needs recorded without excessive sensitive detail or making assumptions? Who may see them?
- **CUS-09** How are family violence, coercion, safety, privacy and safe-contact instructions handled across every channel and document?
- **CUS-10** How does a customer challenge an inaccurate CRM record or request access to it?

## C. Contact and complaint recognition

- **INT-01** What channels receive contact today and in the target: branch, phone, post, email, web, mobile app, chat, social media, third party, AFCA or regulator?
- **INT-02** What exact event counts as receipt in each channel, including after-hours, bounced email, disconnected chat, voicemail and third-party referrals?
- **INT-03** How will staff recognise a complaint even if the customer says "feedback", "question" or "I am disappointed"?
- **INT-04** How is a complaint distinguished from an enquiry, service request, hardship notice, unauthorised-transaction report or chargeback? Can one contact create several linked records?
- **INT-05** Which contacts must be captured even if fixed during the conversation or within five business days?
- **INT-06** Who can create or amend a case, and can a customer lodge anonymously or without authenticating first?
- **INT-07** What minimum fields are required to accept a complaint without imposing an unreasonable barrier?
- **INT-08** How are attachments, call recordings, transcripts, screenshots and paper documents captured, classified and linked?
- **INT-09** How are duplicate contacts, reopened issues, group complaints and several products in one complaint handled?
- **INT-10** What happens if the customer withdraws, cannot be reached, refuses information or uses abusive language?
- **INT-11** What receipt timestamp, timezone, channel, original words and consent/notice evidence must be immutable?
- **INT-12** How does a branch or third-party team hand off a case without resetting the complaint clock?

## D. Journey and case state

- **WF-01** What are the allowed states from intake through closure? What business event moves a case between them?
- **WF-02** Can a case have multiple issues with separate decisions and remedies? Does a parent case close only after every child issue is resolved?
- **WF-03** Which activities can happen in parallel: fraud investigation, account correction, hardship support, complaint review and legal review?
- **WF-04** What evidence is needed to move from triage to investigation, investigation to decision, and decision to implemented outcome?
- **WF-05** What is the definition of "resolved" versus "response sent" versus "outcome implemented" versus "closed"?
- **WF-06** When can a closed case reopen, and does reopening create a new complaint and new clock?
- **WF-07** What happens when the wrong entity, product or team received the complaint? Is it transferred, referred or rejected, and how is the customer informed?
- **WF-08** Which holds or pauses are valid under policy and law? Does any hold alter a regulatory deadline?
- **WF-09** Which state changes need second-person approval or a reason code?
- **WF-10** How are linked incidents, fraud alerts, legal matters and systemic investigations shown without exposing restricted details?

## E. Ownership, queues, priorities and capacity

- **OPS-01** What teams own first contact, specialist investigation, final decision, response, remedy execution and AFCA engagement?
- **OPS-02** What is the single accountable owner when several teams must act? Who takes ownership if a queue is unattended?
- **OPS-03** How are cases assigned: skill, product, geography, language, severity, workload, conflict of interest or customer preference?
- **OPS-04** What urgency factors require immediate action: ongoing loss, fraud, hardship, imminent enforcement, safety, vulnerability or media/regulatory exposure?
- **OPS-05** What are the priority levels, response targets and escalation thresholds? Which are internal targets versus regulatory maximums?
- **OPS-06** How are out-of-hours, leave, handovers, abandoned assignments and team reorganisations handled?
- **OPS-07** What authority may frontline staff exercise for fee refunds, goodwill, compensation, account changes and exceptions?
- **OPS-08** Who reviews a case involving the handling agent, a senior employee or an allegation of misconduct?
- **OPS-09** What staffing forecast follows from arrival volume, case mix, handling effort and rework? What happens at peak demand?
- **OPS-10** What worklist views and alerts do agents, team leads, complaints managers and executives need?

## F. Investigation and evidence

- **INV-01** What facts must be established for each complaint category and which systems supply them?
- **INV-02** Which evidence may be requested from a customer and which should the firm retrieve itself?
- **INV-03** How are conflicting facts, missing records, third-party evidence and contested call recordings handled?
- **INV-04** How are investigation actions, findings, source documents and rationale recorded so another reviewer can reproduce the decision?
- **INV-05** Who may access privileged, fraud, AML, family violence or employee-misconduct material? How is it separated from customer-visible content?
- **INV-06** Which evidence types require original-file preservation, hash, chain of custody or legal hold?
- **INV-07** How are requests to another team tracked with due dates and proof of completion?
- **INV-08** What constitutes sufficient evidence to uphold, partly uphold, reject or offer an ex-gratia outcome?
- **INV-09** What does an independent review require for fairness and conflict-of-interest management?
- **INV-10** How are an investigation mistake and changed decision corrected without erasing history?

## G. Rules, clocks and exceptions

- **RUL-01** Which statutes, regulations, codes, scheme rules, licence conditions and internal policies apply by product, customer, case and date?
- **RUL-02** What is the applicable IDR response deadline for each complaint class, including credit default and hardship variations?
- **RUL-03** Precisely when does each clock start? Which local calendar, public holidays and daylight-saving rules apply?
- **RUL-04** Which clocks are calendar-day and which are business-day? What is the rule when a deadline falls on a non-business day?
- **RUL-05** What earlier internal targets and warning thresholds support meeting each maximum deadline?
- **RUL-06** What information may be missing without delaying acceptance of the complaint?
- **RUL-07** When is a delay notification allowed, what must it contain and who approves it?
- **RUL-08** When can the short-resolution exception apply, and when is a written response still mandatory?
- **RUL-09** Do card-scheme, ePayments, credit or other product-specific processes add separate deadlines?
- **RUL-10** How will rule versions be applied to old and new cases when a regulation or policy changes?
- **RUL-11** How will deadline calculations be tested against weekends, leap days, daylight saving and backdated receipt corrections?
- **RUL-12** Who can change a deadline or override a rule, under what authority, with what audit record and notification?

## H. Customer communications

- **COM-01** What acknowledgements, progress updates, information requests, delay notices, decisions and closure confirmations are needed?
- **COM-02** Which communications must be written, and which can be verbal? What proof of sending and delivery is needed?
- **COM-03** Which templates vary by product, outcome, language, accessibility need, brand and legal entity?
- **COM-04** How will a final response address each issue, evidence, reasons, remedy and AFCA rights without exposing restricted information?
- **COM-05** Who approves wording for rejection, partial rejection, compensation, hardship, fraud and regulatory matters?
- **COM-06** How are bounced messages, wrong addresses, unsafe contact channels and postal delays handled?
- **COM-07** What progress updates are promised internally even if not legally specified? Can the customer choose fewer updates?
- **COM-08** Can customers view case status, upload evidence, correct facts or reply through a portal? Which status detail is safe to reveal?
- **COM-09** What rules control marketing or cross-selling while a complaint is open?
- **COM-10** How are contacts documented when the customer uses an interpreter, advocate or accessible format?

## I. Outcomes, payments and remediation

- **OUT-01** What outcome categories are needed and can several apply to one case?
- **OUT-02** What remedies are available: explanation, apology, fee reversal, refund, interest, compensation, account correction, contract change, service action or debt action pause?
- **OUT-03** Who calculates amounts and approves them at each threshold? Are maker-checker controls needed?
- **OUT-04** What is the authoritative ledger or core system for monetary outcomes? How is the CRM reconciled to executed payment?
- **OUT-05** When is a complaint closed if the customer accepts a remedy but payment or correction is still pending?
- **OUT-06** How are tax, interest, offsets, closed accounts, deceased estates and failed payments handled?
- **OUT-07** What triggers a cohort review or remediation program beyond the individual case?
- **OUT-08** How are affected customers identified, contacted, paid and tracked in a systemic remediation program?
- **OUT-09** How are rejected offers, negotiated settlements and customer acceptance recorded?
- **OUT-10** How are the effect of a remedy and customer satisfaction verified after closure?

## J. External escalation and regulatory interactions

- **EXT-01** How can a customer access AFCA, and what information is given at each relevant point?
- **EXT-02** Who owns AFCA cases, refer-back cases, determinations, evidence requests and implementation of outcomes?
- **EXT-03** How are AFCA reference, dates, status, requested documents and deadline stored and linked to the IDR case?
- **EXT-04** Which data may be supplied to AFCA and which must be redacted or approved first?
- **EXT-05** How are court, regulator, ombudsman, advocate, MP and media contacts routed without losing the original complaint?
- **EXT-06** What is the process for suspected breach reporting, privacy incidents or operational incidents that emerge during a complaint?
- **EXT-07** Who decides whether an issue is systemic, who receives escalation and how are actions and customer cohorts linked?
- **EXT-08** How are regulatory or scheme reporting records reconciled to the underlying complaint population?
- **EXT-09** How are response packs reproduced for audit years after the original case closes?

## K. Data model, taxonomy and quality

- **DAT-01** What entities are required: person, organisation, relationship, product, account, interaction, case, issue, task, evidence, decision, communication, remedy and systemic issue?
- **DAT-02** Which system owns each entity and identifier? Which fields are copied, referenced or queried live?
- **DAT-03** What taxonomy classifies product, service, issue, root cause, outcome, channel, vulnerability and customer segment?
- **DAT-04** Which fields are mandatory at intake, triage, decision and closure, and why?
- **DAT-05** Which values can change and how is previous value, editor, reason and timestamp preserved?
- **DAT-06** How are duplicate cases detected and linked without losing separate receipt dates or complainants?
- **DAT-07** What data quality rules flag impossible dates, missing outcomes, inconsistent classifications or compensation mismatches?
- **DAT-08** What retention schedule applies per record type, including legal holds and deletion/de-identification after lawful need ends?
- **DAT-09** Which data must be searchable, exportable, portable or available for subject access/correction?
- **DAT-10** What are reporting definitions for "received", "open", "closed", "resolved", "overdue" and "reopened"?
- **DAT-11** How are analytics datasets de-identified and how is re-identification risk managed?

## L. Integrations and technical boundaries

- **INTG-01** Which identity, customer, core banking, card, payments, document, telephony, email, chat, branch and fraud systems must connect?
- **INTG-02** For each integration, what business event, data fields, frequency, direction, owner and service level apply?
- **INTG-03** Which operations need real-time data and which can tolerate batch updates?
- **INTG-04** What happens when an upstream system is unavailable, stale or returns conflicting data?
- **INTG-05** How are duplicate events, retries, replay, ordering and idempotency handled for case creation and payments?
- **INTG-06** How is identity matched across brands or legacy systems, and how are false matches corrected?
- **INTG-07** What approval is needed before CRM can write to an account, ledger or customer master?
- **INTG-08** What must be logged at integration boundaries without storing unnecessary personal or secret data?
- **INTG-09** What contracts or API limits apply to third-party systems and what is the fallback?
- **INTG-10** How will integration versions and schema changes be tested and rolled out?

## M. Access, privacy, security and fraud

- **SEC-01** What roles exist and which cases, fields, attachments and actions can each role see or perform?
- **SEC-02** Are entitlements determined by team, product, region, relationship, sensitivity, case assignment or a combination?
- **SEC-03** Which actions require step-up authentication, dual control or an independent approver?
- **SEC-04** How are staff, contractors, service providers and break-glass users onboarded, reviewed and removed?
- **SEC-05** What purposes permit collection and use of each personal-data category? What notices or permissions are required?
- **SEC-06** How will the system prevent disclosure to an abusive partner, impostor or unauthorised representative?
- **SEC-07** Which fields require encryption, tokenisation, masking, redaction or restricted attachment storage?
- **SEC-08** What audit events must be tamper-evident, retained and monitored for unusual access?
- **SEC-09** What data residency, overseas support, subprocessors and cross-border disclosure rules apply?
- **SEC-10** How are suspected privacy breaches, security incidents and fraud indicators identified and escalated?
- **SEC-11** How are test environments, logs, analytics and AI tools protected from real customer data?
- **SEC-12** How will security testing, access recertification and control evidence be maintained?

## N. Reliability, accessibility and service operation

- **NFR-01** What are expected contact volume, concurrent users, attachment size and growth over three years?
- **NFR-02** Which user journeys have response-time targets and at what load percentile?
- **NFR-03** What availability, recovery time and recovery point are needed by operation and channel?
- **NFR-04** What manual continuity procedure is used during CRM, identity, network or core-system outage?
- **NFR-05** How are manually logged complaints back-entered while preserving original receipt and evidence?
- **NFR-06** What browsers, devices, assistive technology and accessibility standards must be supported?
- **NFR-07** What observability is needed for queue growth, failed messages, clock risk, integration errors and payment mismatch?
- **NFR-08** What support hours, incident ownership, on-call and escalation path are required?
- **NFR-09** What backup, restore and disaster-recovery exercises must be demonstrated?
- **NFR-10** What can be configured without code and how are configuration changes approved and audited?

## O. Reporting, governance and improvement

- **REP-01** Which reports are needed daily, weekly, monthly and for board or regulator submission?
- **REP-02** How are complaint volume and rate normalised by active customer, product and channel?
- **REP-03** What metrics expose harm: overdue cases, repeat complaints, unresolved remedies, vulnerability outcomes and rejected decisions later reversed?
- **REP-04** What operational metrics matter: first-contact resolution, age, backlog, rework, transfers and queue dwell time?
- **REP-05** What definitions and exclusions must accompany every metric to prevent misleading comparisons?
- **REP-06** Who can drill from aggregate trends to underlying cases, and how is access controlled?
- **REP-07** Which thresholds trigger root-cause review, policy change, product fix or cohort remediation?
- **REP-08** How will complaints feed product, conduct risk, training and control improvement processes?
- **REP-09** How are dashboard figures reconciled to regulatory submission and source records?
- **REP-10** How are customer feedback and fairness outcomes reviewed, including for vulnerable groups?

## P. AI and automation

- **AI-01** Which use cases are proposed: transcription, summarisation, translation, classification, routing, knowledge retrieval, draft response, QA or trend detection?
- **AI-02** For each use case, is AI advisory or permitted to take action? Who reviews its output before a customer, account or regulator is affected?
- **AI-03** What data can be sent to each AI service, where is it processed and retained, and is it used to train a provider's model?
- **AI-04** What source material may AI cite and how are policy versions controlled?
- **AI-05** How will fabricated facts, missed complaint recognition and incorrect deadlines be detected?
- **AI-06** What evaluation set covers accents, languages, disability, vulnerable customers, ambiguous wording and fraud?
- **AI-07** What explanation and audit record are needed when AI influences a triage or recommendation?
- **AI-08** How can staff override automation, record why and trigger model or rule review?
- **AI-09** How are prompt injection, malicious attachments and inappropriate data leakage prevented?
- **AI-10** What fallback process works if AI is unavailable or confidence is low?
- **AI-11** What monitoring detects drift, bias, rising error rates and changes in source policy?

## Q. Migration, adoption and delivery

- **DEL-01** Which existing cases, documents, notes, recordings and audit logs must migrate, and why?
- **DEL-02** How will open cases retain their original receipt dates, clocks, owner, evidence and customer commitments?
- **DEL-03** What source-data quality problems must be fixed before migration and who accepts residual issues?
- **DEL-04** Will rollout be pilot, product-by-product, channel-by-channel or big bang? What is the rollback plan?
- **DEL-05** What parallel run or reconciliation proves no complaint was lost or double counted?
- **DEL-06** What training and policy changes are needed for frontline staff, specialists, managers and support teams?
- **DEL-07** How will customer-facing policy, forms and communication templates change?
- **DEL-08** What is the acceptance gate for functional, security, privacy, accessibility, performance and disaster-recovery testing?
- **DEL-09** Who owns post-launch defects, rule updates, taxonomy changes and regulatory reviews?
- **DEL-10** What evidence must be retained to prove approval and operation of controls at go-live?

## R. Banking scenario probes

- **BNK-01** If a card transaction is disputed, how is the transaction investigation distinguished from a complaint about the transaction outcome or handling?
- **BNK-02** If a customer alleges a scam or unauthorised payment, what immediate protective actions run independently from complaint investigation?
- **BNK-03** If the customer is in financial difficulty, how do hardship assessment and complaint clocks interact without conflating the two?
- **BNK-04** If debt collection or foreclosure is under way, who decides whether action should pause and how is that instruction enforced?
- **BNK-05** If a fee error affects many customers, what event opens a systemic investigation and how is affected cohort estimated?
- **BNK-06** If family violence is disclosed, what safe-contact, account-access and evidence-handling path applies?
- **BNK-07** If a deceased customer's representative complains, how are authority and information access validated?
- **BNK-08** If one complaint spans a credit card and mortgage, which legal entity and response clock apply to each issue?
- **BNK-09** If an agent offers compensation, how are approvals, ledger posting and customer communication kept consistent?
- **BNK-10** If an AFCA case is referred back while IDR is open or closed, how are records and deadlines linked?
- **BNK-11** If a customer asks for a written response after a fast verbal resolution, what happens?
- **BNK-12** If the issue suggests a privacy or cyber incident, what separate incident process starts and who controls notifications?

## Interview output test

For each relevant question, capture: answer; example case; current policy or data; exception; unresolved decision; owner; approval status; requirement IDs; test scenarios. A statement like "the system should be user-friendly" is incomplete until observable behaviour and a measurable acceptance criterion are defined.
