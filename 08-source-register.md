# Source register: Australian banking complaints

Checked 27 September 2026. These are primary sources used to frame discovery. The source owner should recheck the live publication, applicability and version before approving requirements. A source is not itself a finished system requirement.

| ID | Primary source | Design questions informed | Scope / caution |
| --- | --- | --- | --- |
| AU-01 | [ASIC RG 271, Internal dispute resolution](https://download.asic.gov.au/media/3olo5aq5/rg271-published-2-september-2021.pdf) | Complaint definition, recognition across channels, acknowledgement, IDR response, deadlines, short-resolution exception, governance, accessibility, systemic issues and outcomes | Check the firm's AFS/credit activities and any subsequent amendment. RG 271 distinguishes enforceable paragraphs, guidance and expectations. |
| AU-02 | [ASIC IDR data reporting](https://www.asic.gov.au/regulatory-resources/financial-services/dispute-resolution/internal-dispute-resolution-data-reporting) and [updated IDR data reporting handbook announcement](https://www.asic.gov.au/about-asic/news-centre/news-items/asic-publishes-updated-idr-data-reporting-handbook) | Reporting population, schema, classifications, submission period, corrections and reconciliation | The reporting handbook and instrument can change; implement a versioned export mapping rather than fixed assumptions. |
| AU-03 | [AFCA complaints process](https://www.afca.org.au/make-a-complaint) and [AFCA systemic issues process](https://www.afca.org.au/about-afca/systemic-issues) | External escalation, evidence packs, refer-back, systemic issue handling | Verify AFCA membership, rules, portal process and which complaint types fall within jurisdiction. |
| AU-04 | [APRA CPS 234 Information Security](https://www.apra.gov.au/standards/cps-234) | Information asset classification, security controls, incident escalation, testing and service providers | Applies to APRA-regulated entities; notifications have specific triggers. |
| AU-05 | [APRA CPS 230 Operational Risk Management](https://www.apra.gov.au/standards/cps-230) | Critical operations, tolerance, continuity, service providers and material arrangements | Current in-force standard shown by APRA includes amendments effective 1 July 2026. Determine if the CRM supports a critical operation and which providers are material. |
| AU-06 | [OAIC Australian Privacy Principles](https://www.oaic.gov.au/privacy/australian-privacy-principles/read-the-australian-privacy-principles) and [APP 11 guidance](https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-guidelines/chapter-11-app-11-security-of-personal-information) | Collection, use, access, correction, retention, security and deletion/de-identification | Map each personal-data purpose, legal retention requirement and cross-border disclosure with privacy counsel. |
| AU-07 | [OAIC Notifiable Data Breaches quick reference](https://www.oaic.gov.au/privacy/notifiable-data-breaches/quick-reference-guide-for-responding-to-data-breaches) | Suspected breach detection, assessment, notification and evidence | The 30-calendar-day period concerns assessment of a suspected eligible breach, not a blanket deadline to notify all incidents. |
| AU-08 | [2025 Banking Code of Practice](https://www.ausbanking.org.au/banking-code/) | Customer protections, accessibility, vulnerability, financial difficulty and communications | First verify whether the bank subscribes to this Code and which clauses apply. |
| AU-09 | [ASIC RG 277 Consumer remediation](https://www.asic.gov.au/regulatory-resources/find-a-document/regulatory-guides/rg-277-consumer-remediation) | Linking individual complaints to cohort investigations and remediation | Validate licence and remediation obligations with legal/compliance. |
| AU-10 | [Australian Cyber Security Centre Essential Eight](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/essential-eight) | Security baseline discussion | Useful baseline; it does not replace APRA, privacy or the bank's own security requirements. |

## Specific RG 271 checkpoints for rule owners

- RG 271.27–.35: a qualifying expression of dissatisfaction triggers IDR from receipt, including relevant social media interactions. A hardship request or unauthorised-transaction report alone is not automatically a complaint; separate dissatisfaction about handling or outcome can be.
- RG 271.51–.52: ASIC expects prompt acknowledgement, within 24 hours or one business day where practicable. Capture channel and customer communication preference.
- RG 271.53–.55: a written IDR response has required content, including outcome, AFCA rights and contact details; rejection or partial rejection needs reasons.
- RG 271.56–.60 and Table 2: standard response maximum is 30 calendar days; some credit complaint types have 21-calendar-day rules, and other exceptions or special regimes apply. The clock starts from receipt, not transfer to a specialist team.
- RG 271.64–.66: a permissible delay requires specified circumstances and a notification before the original maximum expires, with reasons and AFCA details.
- RG 271.71–.75: certain complaints closed within five business days need no written IDR response, but the listed exceptions include customer request and hardship. The complaint still needs appropriate capture and reporting.
- RG 271.118–.121: governance and analysis of potential systemic issues; link a confirmed issue to affected-customer remediation.
- RG 271.164–.165: record outcome/remedy and implement agreed resolution outcomes in a timely manner.

## Regulatory rule record

For each rule, record: rule ID; source and paragraph; effective date; applicability rationale; business interpretation; edge cases; clock start/stop and calendar; responsible approver; implementation location; test cases; and next review date. Do not paste a number from a source into code without this record.
