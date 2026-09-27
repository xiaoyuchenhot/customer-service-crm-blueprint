# Customer service CRM requirements repository

**Purpose:** a reusable discovery kit for a company considering its own customer service CRM. The worked example is an Australian bank handling complaints. This repository captures business decisions before anyone asks a developer or AI system to implement them.

**Status:** discovery starter, not an approved bank specification. All example rules and targets need the named business, compliance, privacy, security and technology owners to validate them against the firm's products, licences, policies and current obligations. Research checked on 27 September 2026.

**New to the repository?** Read [START-HERE.md](START-HERE.md). It explains how to use the guided [CRM discovery skill](skills/crm-discovery/SKILL.md) to turn an initial idea into a reviewed [business blueprint](11-business-blueprint-template.md), then into specifications and a bounded implementation slice.

## What to do first

1. Name a business sponsor, complaints policy owner, compliance owner, privacy owner, security owner, data owner and solution architect.
2. Complete the scope and operating model questions in [01-discovery-question-bank.md](01-discovery-question-bank.md). Record answers and evidence using [03-workshop-capture-template.md](03-workshop-capture-template.md).
3. Select journeys from [10-service-scenario-catalog.md](10-service-scenario-catalog.md). Map at least a simple service request, a complaint resolved at first contact, and a complex complaint with an external escalation. Include channel handoffs and exceptions.
4. Use [02-banking-complaints-example.md](02-banking-complaints-example.md) as a **worked example**, then replace assumptions with the firm's decisions.
5. Convert approved answers into [04-brd-template.md](04-brd-template.md) and [05-functional-spec-template.md](05-functional-spec-template.md).
6. Use [06-traceability-register.csv](06-traceability-register.csv) to connect each requirement to a source, owner, test and release. Use [07-ai-prompt-playbook.md](07-ai-prompt-playbook.md) only with approved, appropriately redacted material.
7. Review current primary sources in [08-source-register.md](08-source-register.md) before accepting regulatory rules or implementation.

## Core distinction

| Artefact | Main question it answers | Typical approver |
| --- | --- | --- |
| Discovery notes | What happens today and what remains unknown? | Process owner |
| Business requirements document (BRD) | Why change, who is affected, what outcomes and rules are required? | Sponsor, operations, compliance |
| Functional specification | Exactly what should users and systems do in every state and exception? | Product owner, operations, architecture |
| Nonfunctional and control specification | How secure, reliable, accessible, observable and recoverable must it be? | Security, privacy, operations, architecture |
| Traceability register | Which source, decision, design and test prove each requirement? | Product owner, test lead |
| Decision log | Why was a design or policy choice made, by whom and when? | Accountable owner |

## Suggested bounded first release

Start with intake from phone, web and email; complaint recognition; case creation; customer and product linkage; ownership and queues; deadlines; acknowledgements; investigation notes and evidence; response approval; outcome execution; audit trail; basic reporting; and manual AFCA handoff. Add more channels, automated triage and advanced analytics after the operating rules are proven. The release boundary is a planning example, not a vendor or architecture recommendation.

## Repository conventions

- Mark each statement **Confirmed**, **Proposed**, **Assumption** or **Open**.
- Give every requirement an ID and one accountable business owner.
- Record the jurisdiction, source URL, source version/date, interpretation owner and review date for every regulatory rule.
- Keep regulatory maximums separate from internal service targets.
- Store real customer data and secrets outside this repository. Use synthetic examples in prompts and tests.
- Track unresolved questions as decisions, including the consequence of leaving them unresolved.

## Completion gate before development

A feature is ready for implementation when its trigger, actor, preconditions, normal flow, alternate flows, data, permissions, external dependencies, time rules, acceptance tests, operational owner and source are approved. Any missing item must be explicitly listed as an open decision; AI output cannot silently supply it.
