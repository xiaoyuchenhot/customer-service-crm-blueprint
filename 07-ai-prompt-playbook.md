# AI prompt playbook: from interviews to implementation

AI is most useful when the input is an approved set of decisions and examples. It may draft, organise and challenge a specification; the named owners decide policy and legal interpretation. Replace bracketed placeholders. Use synthetic data unless the organisation has explicitly approved a secure environment and data-sharing arrangement.

## Common instruction to prepend

> You are assisting with requirements for an Australian customer-service CRM. Use only the supplied sources and approved decisions for factual claims about this organisation. Separate Confirmed, Proposed, Assumption and Open items. Preserve source IDs and quote or pinpoint the source for every regulatory rule. Do not invent policies, legal timeframes, customer data, APIs or system-of-record ownership. When information is missing, produce a decision question with options and consequences. Keep regulatory maximums distinct from internal service targets. Return requirement IDs, acceptance criteria and traceability. Flag privacy, security, accessibility, vulnerability and human-review impacts.

## Prompt 1: turn workshop notes into a decision inventory

> Inputs: [paste redacted workshop record, existing policies, source IDs and dates]. Extract only the decisions actually made. Return a table with question ID, exact decision, status, evidence quote/section, accountable owner, effective date, unresolved ambiguity and proposed requirement ID. Put contradictory answers in a separate conflict table. Do not infer agreement from silence.

## Prompt 2: find missing business questions

> Inputs: [scope statement], [completed question-bank answers], [three synthetic journeys]. Compare the answers with the question bank and the journeys. Identify missing decisions that would change customer outcome, complaint classification, ownership, deadline, remedy, privacy, external escalation or reporting. Rank by consequence of getting it wrong. For each, give the person or function best placed to answer and one concrete scenario to test it.

## Prompt 3: model a journey and decision table

> Inputs: [approved rules and scope]. Draft a customer journey and a state-transition table for [scenario]. For each transition include trigger, actor, precondition, data created, permission, clock effect, customer communication, audit event and exception. Keep linked workflows separate when they have different clocks. Mark every unapproved choice as Proposed.

## Prompt 4: draft the BRD

> Inputs: [approved discovery register], [baselines], [scope], [source register]. Fill the BRD template. Make each business requirement measurable and technology-neutral. Provide an assumptions/dependencies table and a list of missing sign-offs. Do not convert a source guideline into a firm obligation without the compliance owner's interpretation.

## Prompt 5: draft the functional specification

> Inputs: [approved BRD requirement IDs], [approved rule records], [target integrations], [role matrix]. Fill the functional specification template for [one capability]. Include normal, alternate and failure flows; data dictionary; state and clock rules; access controls; audit events; notifications; and Given/When/Then tests. Show a traceability table. If an API or field is unknown, state a required interface decision rather than inventing it.

## Prompt 6: challenge the design as a reviewer

> Review this specification as a complaints operations lead, a vulnerable-customer specialist, a privacy officer, a security engineer, a reporting owner and an SRE. List only material gaps or contradictions, each with evidence, likely consequence, affected requirement ID and the exact clarification needed. Test fast resolution, partial rejection, hardship, card disputes, AFCA escalation, systemic issues, unsafe contact, outages and failed remedies.

## Prompt 7: compare architecture options

> Inputs: [approved capability map, nonfunctional targets, integrations, budget horizon, data residency rules and operating constraints]. Compare configure-a-platform, compose-existing-services and custom-build options. For each show fit by capability, integration complexity, security/privacy responsibilities, operational burden, migration, vendor dependence, cost drivers and exit path. Recommend a bounded first release and list assumptions. Do not make a pricing claim without a current dated source.

## Prompt 8: produce an implementation slice

> Inputs: [approved functional spec for one slice], [repository conventions], [approved technology choices]. Create only the code and infrastructure needed for this slice. First list interfaces, state transitions and tests to implement. Preserve immutable receipt and audit history. Use synthetic fixtures. Treat deadlines and response exceptions as versioned policy configuration with tests; do not hardcode a single 30-day rule for every case. Show files changed, test results and any requirement that remains unsupported.

## Prompt 9: generate meaningful tests

> Inputs: [requirement IDs], [rule table], [interface contracts]. Build tests that would catch real mistakes: complaint captured at first contact, no clock reset on transfer, business-day/calendar-day differences, written-response exception, partial rejection content, failed remedy reconciliation, safe-contact restrictions, permissions, duplicate events and outage re-entry. Link each test to requirement and source. Identify tests that cannot be written because behaviour is not decided.

## Prompt 10: release evidence and change impact

> Inputs: [requirements, implementation diff, test results, source versions and open decisions]. Produce a release-readiness report: requirement coverage, unresolved gaps, changed rules, data migration/reconciliation, security/privacy findings, accessibility, operational runbooks, rollback, owner sign-offs and residual risk. For each changed regulation or policy source, identify affected cases, configuration, templates, reports and tests.

## Example prompt for the banking complaint slice

> Use the common instruction. Source requirements: FR-001 through FR-008 in the worked example, but only those the bank has approved. Scenario: a customer phones on Sunday to complain about a repeated mortgage fee, then requests a written response. Produce a state model and acceptance tests. Preserve Sunday receipt. Explain the applicable clock by citing the approved rule record. Include a safe-contact check before sending. If the bank has not specified its public-holiday calendar, response template or refund approval authority, output explicit open decisions.

## Review rules for AI output

Reject or revise output if it invents an internal policy; conflates transaction disputes/hardship requests with complaints; treats every case as a 30-day case; resets the clock on transfer; treats a workflow hold as a legal clock pause; omits AFCA rights from a required response; closes a case while a remedy is unexecuted without an approved closure rule; exposes sensitive notes; or cannot trace a requirement to an approved decision.
