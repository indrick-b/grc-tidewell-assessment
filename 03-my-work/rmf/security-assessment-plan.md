# Security Assessment Plan (SAP) — Tidewell CUI Environment

> Practice document. The SAP is written **before** testing. It says what will be tested, how, by whom, and when, so leadership and the people being assessed agree on the rules up front.

| Field | Value |
| --- | --- |
| Assessment | Tidewell security assessment against NIST SP 800-171 Rev. 2 (with CSF, 800-53, SOC 2, ISO 27001, CIS mappings) |
| Assessor | Indrick Bodkin, GRC Analyst |
| Sponsor | Priya Natarajan, CFO |
| Fieldwork dates | October 27 – November 4, 2026 |
| Assessment date (as-of date for all results) | November 2, 2026 |

## 1. Scope
**In scope:** *List the systems from the SSP boundary (section 3).*
**Out of scope:** PRINT01 (print server, no CUI); SecureShred Tampa paper shredding operations. *Add anything else and explain why.*

## 2. What's being tested
The 26 controls in [`../../02-framework/control-checklist.csv`](../../02-framework/control-checklist.csv), which cover the NIST SP 800-171 requirements listed in SSP section 6.

## 3. Methods
Each control is tested using one or more of the NIST SP 800-171A methods: **Examine** (documents, settings, records), **Interview** (people who run the control), and **Test** (exercise the control and check the result). The method for each control is in the `test_method` column of the checklist.

## 4. Sampling
*When there are too many items to check one by one, you check a sample. Fill in how you sampled for each of these. "All" is a fine answer when the population is small.*

| Population | Size | Sample size | How chosen | Why |
| --- | --- | --- | --- | --- |
| Personnel files (background checks) | 62 employees | 5 | | |
| Terminated employees (account removal) | 9 | All 9 | Full population | Small enough to check every one |
| Laptops (encryption, patching, EDR) | 48 | | | |
| Backup jobs | 93 jobs (October 2026) | | | |
| LedgerPoint users | 12 | | | |

## 5. Evidence request list
Evidence requested from Tidewell staff is tracked in [`../evidence-request-list.csv`](../evidence-request-list.csv).

## 6. Rules of engagement
- The assessor will view settings and exports but will **not** change any system.
- If the assessor finds something that needs immediate action (for example, an active compromise or a terminated employee who still has access), they will tell the CFO and IT Manager the **same day**, before the report is final.
- Findings describe control failures, not individual blame.
- Draft findings will be shared with each control owner to confirm the facts before the report goes to leadership.

## 7. Schedule
| Date | Activity |
| --- | --- |
| Oct 27–31 | Interviews |
| Oct 31–Nov 4 | Evidence review and testing |
| | Draft findings reviewed with control owners |
| | SAR and executive summary delivered |

## 8. Approval
| Role | Name | Date |
| --- | --- | --- |
| Assessor | Indrick Bodkin | |
| Sponsor | Priya Natarajan, CFO | |
