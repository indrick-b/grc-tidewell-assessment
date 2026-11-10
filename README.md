# GRC Security Assessment: Tidewell Logistics (Practice Project)

A full governance, risk, and compliance (GRC) assessment of a fictional 62-person logistics company that serves **both** a defense prime contractor and commercial customers. It works through the same tasks a GRC analyst does on the job: gathering evidence, testing controls, writing findings, rating risk, building a POA&M, updating policy, answering a customer security questionnaire, and briefing leadership.

> **About this project:** Tidewell Logistics and everything about it is fictional. The scenario and evidence files were built with AI assistance to simulate a realistic environment. The assessment work in [`03-my-work/`](03-my-work/), including the control testing, findings, risk ratings, POA&M, policy rewrite, questionnaire answers, and executive summary, is my own.

## The situation

In September 2026, a phishing email let an attacker into an employee's mailbox, which had no MFA. The attacker sent a fake invoice, and a customer paid **$48,500** to the attacker. Nobody followed an incident plan, checked for exposed CUI, or notified the prime contractor. Three deadlines followed:

| Deadline | Who | What they need |
| --- | --- | --- |
| Dec 15, 2026 | Brightwater Retail (largest customer) | Security questionnaire + SOC 2 plan |
| Jan 15, 2027 | Harborline Mutual (cyber insurer) | Proof of MFA, tested backups, training |
| Feb 1, 2027 | Northstar Defense (prime contractor) | NIST 800-171 SSP, POA&M, SPRS score |

Full story: [`00-scenario/`](00-scenario/)

## Frameworks used

One assessment, mapped to four frameworks, so it applies to both the government and private sectors:

- **NIST SP 800-171 Rev. 2** and **DFARS 252.204-7012** (defense contractors handling CUI; CMMC Level 2)
- **NIST SP 800-53 Rev. 5** (federal systems, RMF)
- **NIST Cybersecurity Framework 2.0** (common language for leadership)
- **SOC 2 Trust Services Criteria** (commercial customers)
- **NIST SP 800-63B-4** (password and authentication guidance)

## What's in this repo

| Folder | Contents |
| --- | --- |
| [`00-scenario/`](00-scenario/) | Company profile and the incident |
| [`01-evidence/`](01-evidence/) | Interview notes, current policies, system exports (CSV), and outside requests |
| [`02-framework/`](02-framework/) | 23-control checklist mapped across all four frameworks |
| [`03-my-work/`](03-my-work/) | My findings, risk register, POA&M, new policy, questionnaire answers, and executive summary |

## Skills shown

| On-the-job GRC task | Where it happens in this project |
| --- | --- |
| Collect and review evidence | Interview notes, policy review, CSV analysis (for example, matching HR terminations to active AD accounts) |
| Test controls against a framework | `control-checklist.csv` |
| Write audit findings | `findings.md` (condition, criteria, cause, effect, recommendation) |
| Assess and rate risk | `risk-register.csv` (likelihood × impact) |
| Track remediation | `poam.csv` (POA&M format used for NIST 800-171 and FedRAMP) |
| Write and update policy | `password-policy-v2.md` |
| Answer customer security questionnaires | `brightwater-answers.md` |
| Communicate risk to leadership | `executive-summary.md` |
