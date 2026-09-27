# Start here: use this repository to discover and design a customer-service CRM

This guide is for a founder, business sponsor, product owner or analyst who starts with an idea such as **"I want to build a CRM for customer service."** The repository provides a structured conversation and durable project documents. It does not require the person to answer 189 questions at once.

The worked example is an Australian bank handling complaints. The same method works for other industries if the team replaces the banking rules, scenarios and sources with those that apply to its business.

## What this repository does

The [discovery skill](skills/crm-discovery/SKILL.md) guides an AI assistant to ask the next useful questions, record answers and gaps, and gradually assemble a [business blueprint](11-business-blueprint-template.md). The [question bank](01-discovery-question-bank.md) is a menu of prompts, not a form to complete from top to bottom. The [scenario catalog](10-service-scenario-catalog.md) helps choose journeys. The [BRD](04-brd-template.md), [functional specification](05-functional-spec-template.md), [architecture log](09-architecture-and-delivery-decisions.md) and [traceability register](06-traceability-register.csv) turn approved decisions into work that a delivery team can verify.

An AI assistant can maintain these files while a project is open in its workspace. The skill is a repeatable **conversation workflow**, not a background service or a finished CRM application. A business owner still approves policy and scope; compliance, privacy and security owners validate obligations and controls; architects and developers decide and implement the system design.

## First use: five steps

1. **Open or clone this repository in Codex or another coding assistant that can read local files.** Work from the repository root so it can see [AGENTS.md](AGENTS.md) and the skill.
2. **Start a project.** Give the assistant your company, industry, jurisdiction, customer-service goal and any known scope. If unsure, say so; the skill will begin with discovery.
3. **Answer a small batch of questions.** The assistant should ask up to five high-value questions, explain why they matter, and accept "unknown" as an answer. It records each answer as Confirmed, Proposed, Assumption or Open.
4. **Review the updated files.** Each round should update a project brief, an answer/decision log, open questions and a business blueprint under a new project folder. Corrections to an answer should update the record, not leave competing versions.
5. **Repeat until a bounded first release is ready.** Then ask the assistant to draft the BRD, functional specifications, test scenarios and architecture options from approved answers. Have the named owners review the documents before implementation.

### Copyable first prompt

> Use the CRM discovery workflow in skills/crm-discovery/SKILL.md. I want to create a customer-service CRM for [company or type of company] in [country]. Our first use case is [complaints / enquiries / service requests / other]. Create a project folder named [short-name], record what I have said as initial context, and ask me the first small batch of questions. Keep unconfirmed assumptions separate from decisions. Do not start coding yet.

For the Australian banking example:

> Use the CRM discovery workflow in skills/crm-discovery/SKILL.md. Start a project called retail-bank-complaints for an Australian retail bank. The goal is to manage customer complaints across phone, branch, web and email. Begin discovery, use the banking worked example only as a reference, and ask me the highest-value questions. Record unknowns explicitly. Do not treat example requirements as my bank's policy.

### Copyable continuation prompt

> Continue discovery for projects/[short-name]. Read the latest project brief, answers, decisions and blueprint. Summarise what is settled, identify the most consequential gaps, ask the next small batch of questions, and update the files after I answer.

### Copyable transition prompt

> Review projects/[short-name] for first-release readiness. Show unresolved decisions by business consequence. From only the approved decisions, draft the BRD and functional specifications for the bounded first release. Link every requirement to its answer or source and propose acceptance tests. Keep assumptions and regulatory interpretations awaiting owner approval visible.

## The conversation in practice

**User:** "I want a CRM for bank customer complaints."

**Assistant, first round:** "Which legal entity and products are in scope? What contact channels receive complaints today? What existing customer and case systems must remain authoritative? Who owns the complaints policy? What customer or operational problem are you trying to improve first?"

**User:** "Retail banking, cards and home loans. Phone and email first. We have a core banking system, but no single case system. We miss follow-ups. Our complaints manager owns policy."

**Assistant:** Records those answers with status and source, notes that the legal entity and exact products remain open, drafts a bounded intake/follow-up problem statement, then asks the next questions about complaint recognition, ownership, clocks and customer communications. It should not assume a single deadline for every banking case or select a technology stack.

## Project files created during discovery

For each initiative, use a separate folder such as **projects/retail-bank-complaints/**:

| File | Purpose | Updated when |
| --- | --- | --- |
| 01-project-brief.md | Problem, outcomes, scope, people, systems and baseline | When scope or objective changes |
| 02-discovery-log.md | Question IDs, answers, evidence, status and dates | After each question round |
| 03-decisions.md | Approved choices, rejected options, owner and effective date | When an accountable person decides |
| 04-open-questions.md | Missing facts ranked by consequence, owner and next action | After each question round |
| 05-business-blueprint.md | Living design of journeys, policies, data, controls and first release | When answers are sufficiently grounded |
| 06-readiness-review.md | Coverage, contradictions, approvals and handoff criteria | Before BRD/specification and before build |

The assistant can make these files on the first round. There is no need to copy every generic template into every project.

## Discovery stages and review gates

| Stage | Questions to settle | Main output | Gate to proceed |
| --- | --- | --- | --- |
| 0. Charter | Why build, for whom, outcomes, legal entity, first release | Project brief | Sponsor agrees on problem and scope |
| 1. Service model | Contact types, channels, customer authority, journeys, handoffs | Journey maps and taxonomy | Operations owner verifies real examples |
| 2. Complaint and policy rules | What counts as a complaint, clocks, communications, remedies, escalation | Rule and decision records | Policy/compliance owner validates applicability |
| 3. Data and controls | Source systems, personal data, access, retention, reporting, resilience | Data/control sections of blueprint | Data, privacy, security and operations review |
| 4. Delivery design | Build/configure/buy, integrations, migration, release slices | Architecture decisions and backlog | Sponsor and architecture approve trade-offs |
| 5. Build handoff | Detailed behaviour, exceptions, acceptance tests and traceability | BRD, specs and test plan | Named owners approve a bounded implementation slice |

These gates are review points, not an instruction to stop asking useful questions on unrelated topics. The assistant can advance independent work while a decision is pending.

## What a good blueprint contains

Use [11-business-blueprint-template.md](11-business-blueprint-template.md). It should answer:

- Who are the customers and staff, and what customer outcomes matter?
- Which service scenarios and channels are in scope?
- What event creates a case and starts each clock?
- What are the lifecycle, roles, handoffs, exceptions and safe-contact paths?
- How are evidence, decisions, responses, remedies and external disputes handled?
- Which systems own customer, account, transaction, case, document and payment data?
- What security, privacy, accessibility, reporting and resilience controls are required?
- What is in the first release, what follows, and what remains an open decision?
- Which requirements and tests trace to each approved answer or authoritative source?

The blueprint is **living** during discovery. The BRD states business outcomes and rules; the functional specification makes one approved capability precise enough to build and test. A code-generation prompt should come only after those decisions are traceable.

## How to use GitHub while the project is young

- Keep the generic question bank, skill and templates on the main branch. Create a separate project folder for each company or product initiative.
- Make one focused change per branch and pull request, for example "define complaint intake and ownership" or "approve hardship clock mapping." The pull request records the decision, reviewers and source changes.
- Ask the relevant owner to review the sections they understand: operations for journeys, compliance for rules, privacy/security for controls, data owners for definitions, and architecture for interfaces and resilience.
- Use issues for decisions with an owner and due date. Put the final answer back into the project decision record so the repository remains the source of truth.
- Keep customer names, account numbers, call recordings, credentials and production exports out of GitHub and AI prompts. Use synthetic or approved redacted examples. A private repository still needs access controls.
- Tag or otherwise identify an approved blueprint version before a release. A new policy interpretation should update its source record, affected requirements, tests and rollout decision.

## When the team can ask AI to build

Choose one bounded implementation slice, such as complaint intake and ownership. Confirm its actor, trigger, original receipt, state transitions, data definitions, permissions, integration contracts, time rules, exceptions, customer messages, operational fallback and acceptance tests. The [AI prompt playbook](07-ai-prompt-playbook.md) then helps request a design review, implementation and tests. Do not ask AI to fill an absent policy decision with a plausible guess.

## Limits to remember

The repository is a discovery and design toolkit. It does not itself interview stakeholders, maintain a live integration, calculate a bank-approved deadline table or deploy a CRM. The banking material is an example. Before live use, the relevant firm must validate applicability and current versions of its law, licence conditions, scheme rules, banking code, internal policies and service-provider obligations using the [source register](08-source-register.md).
