# GRC Security Assessment: Tidewell Logistics (Practice Project)

A full governance, risk, and compliance (GRC) assessment of a fictional 62-person logistics company that serves **both** a defense prime contractor and commercial customers. It works through the tasks a GRC analyst does on the job: collecting evidence, testing controls, scoring risk, writing the federal RMF paperwork (FIPS 199, SSP, SAP, SAR, POA&M), reviewing vendors, running a user access review, searching logs in Splunk, rewriting policy, and briefing leadership.

> **About this project:** Tidewell Logistics and everything about it is fictional. The scenario and evidence files were built with AI assistance to simulate a realistic environment with problems hidden in it. The assessment work in [`03-my-work/`](03-my-work/) is my own: the control testing, findings, risk ratings, POA&M, RMF documents, vendor review, access review, Splunk investigation, policies, and executive summary.

## The situation

In September 2026, a phishing email let an attacker into an employee's mailbox, which had no MFA. The attacker sent a fake invoice, and a customer paid **$48,500** to the attacker. Nobody followed an incident plan, checked for exposed CUI, or notified the prime contractor. Three deadlines followed:

| Deadline | Who | What they need |
| --- | --- | --- |
| Dec 15, 2026 | Brightwater Retail (largest customer) | Security questionnaire + SOC 2 plan |
| Jan 15, 2027 | Harborline Mutual (cyber insurer) | Proof of MFA, tested backups, training |
| Feb 1, 2027 | Northstar Defense (prime contractor) | NIST 800-171 SSP, POA&M, SPRS score |

Full story: [`00-scenario/`](00-scenario/)

## Frameworks and rules used

One set of 26 controls, mapped to six frameworks, so the work applies to both the government and private sectors:

- **Government:** NIST SP 800-171 Rev. 2, DFARS 252.204-7012, CMMC Level 2, NIST SP 800-53 Rev. 5, NIST RMF (SP 800-37), FIPS 199 / SP 800-60
- **Private sector:** SOC 2 Trust Services Criteria, ISO/IEC 27001:2022, CIS Controls v8.1
- **Both:** NIST Cybersecurity Framework 2.0, NIST SP 800-63B-4 (passwords), NIST SP 800-61 (incident response)
- **Laws checked for applicability:** Florida Information Protection Act, PCI DSS, HIPAA, GDPR, SOX ([which apply and which don't](02-framework/regulatory-applicability.md))

## What's in this repo

| Folder | Contents |
| --- | --- |
| [`00-scenario/`](00-scenario/) | Company profile, the incident, and the judgment calls |
| [`01-evidence/`](01-evidence/) | 5 interviews, 3 outdated policies, 13 system exports (including a 1,700-event sign-in log for Splunk), vendor documents, and 3 outside requests |
| [`02-framework/`](02-framework/) | 26-control checklist mapped across six frameworks with test procedures, plus a regulatory applicability worksheet |
| [`03-my-work/`](03-my-work/) | My assessment: findings, risk register, POA&M, RMF package, vendor review, access review, Splunk investigation, policies, communications, and the Excel workbook |

## Skills shown

| GRC analyst skill | Where it happens in this project |
| --- | --- |
| 1. Risk assessment and prioritization | [`risk-register.csv`](03-my-work/risk-register.csv): likelihood × impact, inherent vs. residual risk, treatment decisions; heat map in the workbook |
| 2. Security frameworks and regulations | [`control-checklist.csv`](02-framework/control-checklist.csv) (6 frameworks), [`regulatory-applicability.md`](02-framework/regulatory-applicability.md) |
| 3. Federal RMF and authorization documents | [`rmf/`](03-my-work/rmf/): FIPS 199 categorization, SSP, SAP, SAR with SPRS score estimate, [`poam.csv`](03-my-work/poam.csv) with full lifecycle tracking |
| 4. Control testing and audit support | Examine / Interview / Test procedures for each control, sampling plan in the SAP, [`evidence-request-list.csv`](03-my-work/evidence-request-list.csv), [`findings.md`](03-my-work/findings.md) in condition-criteria-cause-effect format |
| 5. Policy writing | [`password-policy-v2.md`](03-my-work/password-policy-v2.md) (NIST SP 800-63B-4), [`incident-response-plan-v2.md`](03-my-work/incident-response-plan-v2.md) (DFARS 72-hour and Florida 30-day notices) |
| 6. Explaining risk to non-technical people | [`executive-summary.md`](03-my-work/executive-summary.md), [`stakeholder-communications.md`](03-my-work/stakeholder-communications.md) (one risk, three audiences), [`brightwater-answers.md`](03-my-work/brightwater-answers.md) |
| 7. Third-party and vendor risk | [`vendor-risk-assessment.md`](03-my-work/vendor-risk-assessment.md): vendor tiering, MSP questionnaire review, contract terms for legal and procurement, SOC 2 report review (exceptions, CUECs, bridge letter) |
| 8. Data analysis in Excel | [`Tidewell-GRC-Workbook.xlsx`](03-my-work/Tidewell-GRC-Workbook.xlsx): lookup formulas comparing HR to AD/M365/finance, COUNTIFS heat map, dashboard, SPRS calculator |
| 9. GRC platforms and security tools | [`splunk-investigation.md`](03-my-work/splunk-investigation.md): SPL searches on M365 sign-in logs to prove whether controls worked; the workbook is organized like a GRC platform (controls → evidence → findings → risks → POA&M → vendors) |
| 10. Access control and judgment | [`user-access-review.csv`](03-my-work/user-access-review.csv) (AD, finance system, CUI share, payroll portal), separation-of-duties testing, [`judgment-calls.md`](03-my-work/judgment-calls.md) |
