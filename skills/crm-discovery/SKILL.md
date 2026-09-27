---
name: crm-discovery
description: Guide an early customer-service CRM idea through iterative business discovery, decisions and a build-ready blueprint. Use when a user wants to define or refine CRM requirements before implementation.
---

# CRM discovery

Turn a vague service-system idea into a traceable business blueprint through short conversations. Work in the current project repository. Read [START-HERE.md](../../START-HERE.md) for the project file contract and [11-business-blueprint-template.md](../../11-business-blueprint-template.md) for the output shape.

## Start or resume

1. Identify the current project folder from the user's request. If none exists, create projects/<short-name>/ with a brief, discovery log, decisions, open questions and blueprint. Use a neutral short name if needed.
2. Read existing project files before asking a repeated question. Preserve earlier approved decisions and update them when the user corrects them.
3. Start with the objective, company/legal entity, jurisdiction, customer segments, service scenarios, channels and current systems. Use the [question bank](../../01-discovery-question-bank.md) and [scenario catalog](../../10-service-scenario-catalog.md) selectively; do not recite them in full.
4. Ask up to five questions per round, ranked by how much each answer changes customer outcome, policy, architecture or first-release scope. Explain a consequential ambiguity briefly. Accept "unknown" and record the owner needed to resolve it.
5. After each response, update the files with answer, question ID, status (Confirmed / Proposed / Assumption / Open), evidence or source, owner and date. Update the living blueprint only as far as the answers support it. State what changed and ask the next useful batch if the conversation continues.

## Build the blueprint

Cover service journeys, case taxonomy and lifecycle, authority and access, handoffs, clocks and policy exceptions, communications, evidence, outcomes, remedies, external escalation, systemic issues, data and integrations, privacy/security, accessibility, resilience, reporting, migration and delivery. Branch into a topic when scope or a realistic scenario makes it relevant.

For Australian banking complaints, consult the [worked example](../../02-banking-complaints-example.md) and [primary-source register](../../08-source-register.md). Distinguish a complaint from a related hardship request or transaction report. Record the exact source, applicability and policy-owner interpretation for each proposed rule. A source citation or example does not make a rule approved for the user's firm.

Use realistic, synthetic scenarios to challenge each journey. Identify normal, exception, failure and vulnerable-customer paths. Ask the business to choose policy and ownership; ask architecture to choose technical means against approved requirements. Do not invent interfaces, targets or monetary authority.

## Handoff

When the user asks for a BRD, specification, architecture or code, first show coverage and unresolved consequential decisions. Continue work that does not depend on them. Draft the [BRD](../../04-brd-template.md) and [functional specification](../../05-functional-spec-template.md) from approved answers, with requirement IDs, acceptance tests and [traceability](../../06-traceability-register.csv). Use the [AI prompt playbook](../../07-ai-prompt-playbook.md) for bounded implementation slices. Label any unapproved requirement explicitly; do not silently promote it into code.

The work is ready for a first build slice when its actor, trigger, state, data, permissions, external dependencies, time rules, customer communication, exceptions, operational owner and tests are decided and linked to an approver. Keep confidential customer material out of repository files and prompts unless the user provides an approved handling environment.
