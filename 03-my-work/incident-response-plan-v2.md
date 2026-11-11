# Tidewell Logistics — Incident Response Plan (DRAFT v2.0)

> Draft written by the GRC Analyst to replace the 2019 plan. Fill in each section. Use the September incident as your test: if this plan had existed, would it have caught every step that was missed?

| Field | Value |
| --- | --- |
| Version | 2.0 (draft) |
| Plan owner | |
| Approved by | |
| Effective date | |
| Next review | |
| Next test (tabletop exercise) | |
| Replaces | Incident Response Plan v1.0 (February 4, 2019) |

## 1. Purpose and scope
*What counts as an incident? Include: phishing with a stolen password, a mailbox rule set by an attacker, a lost laptop, ransomware, a vendor breach, a terminated employee who still has access, and fraud involving payments or bank details.*

## 2. Incident response team
*Use current people. The 2019 plan named someone who left. Include a backup for each role, and the outside contacts (Bayside, insurer, lawyer).*

| Role | Primary | Backup | Phone |
| --- | --- | --- | --- |
| Incident lead | | | |
| Technical lead | | | |
| Communications / leadership | | | |
| Legal counsel | | | |
| Government contract contact (for Northstar) | | | |

## 3. Severity levels
| Level | Example | Who must be told, and how fast |
| --- | --- | --- |
| 1 — Low | | |
| 2 — Medium | | |
| 3 — High | *Any incident that may involve CUI, personal information, or money* | |

## 4. Steps (follow NIST SP 800-61 phases)
1. **Detect and report.** *How does an employee report something? How fast?*
2. **Analyze.** *Questions to answer before closing: What data was in the attacker's reach? Was CUI involved? Personal information? Were any inbox rules, forwarding rules, or bank details changed?*
3. **Contain.** *For example: disable the account, revoke sessions, reset the password, require MFA, block the sender.*
4. **Eradicate and recover.**
5. **Notify.** *Fill in the table below.*
6. **Lessons learned.** *Within how many days? Who writes it up?*

## 5. Notification requirements
| Who | When required | Deadline | Who sends it |
| --- | --- | --- | --- |
| DoD, via the DIBNet portal (DFARS 252.204-7012) | Cyber incident affecting covered defense information (CUI) or the ability to perform the contract | 72 hours from discovery | |
| Northstar Defense Services | Same as above (subcontract flow-down) | | |
| Harborline Mutual (insurer) | *Check the policy* | | |
| Affected individuals in Florida (Fla. Stat. § 501.171) | Breach of personal information | No later than 30 days after determining a breach | |
| Florida Attorney General's office | Same, if 500+ Floridians affected | 30 days | |
| Affected customers | *Business decision. Who decides?* | | |

*DFARS also requires preserving images of affected systems and relevant monitoring data for at least 90 days after the report. Add how Tidewell will do that.*

## 6. Testing
*How often will Tidewell run a tabletop exercise, and who attends? Suggest a first scenario.*

## 7. Compliance mapping
| Requirement | Framework reference |
| --- | --- |
| Have an incident response plan | NIST 800-171 3.6.1 · NIST 800-53 IR-8 · ISO 27001 A.5.24 · SOC 2 CC7.4 |
| Report incidents | NIST 800-171 3.6.2 · NIST 800-53 IR-6 · DFARS 252.204-7012(c) |
| Test the plan | NIST 800-171 3.6.3 · NIST 800-53 IR-3 · CIS 17.7 |

## 8. Revision history
| Version | Date | Author | Change |
| --- | --- | --- | --- |
| 1.0 | 2019-02-04 | R. Sutter | Original plan |
| 2.0 | | Indrick Bodkin | Rewritten after the September 2026 incident |
