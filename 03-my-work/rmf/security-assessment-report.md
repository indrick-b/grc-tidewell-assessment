# Security Assessment Report (SAR) — Tidewell CUI Environment

> Practice document. The SAR is written **after** testing. It says what was found. The executive summary is the one-page version for leadership; this is the full version for Northstar, auditors, and the IT team.

| Field | Value |
| --- | --- |
| Assessment | See [`security-assessment-plan.md`](security-assessment-plan.md) |
| Assessment date | November 2, 2026 |
| Report date | |
| Assessor | Indrick Bodkin, GRC Analyst |

## 1. Summary of results
| Result | Number of controls |
| --- | --- |
| Met | |
| Partially met | |
| Not met | |
| **Total tested** | **26** |

## 2. Results by control
*Copy the status and evidence notes for each control from the checklist. Link each Partially met or Not met to its finding.*

| Control | Requirement (short) | Status | Finding | Risk rating |
| --- | --- | --- | --- | --- |
| TW-01 | Password policy follows current NIST guidance | Not met | F-01 | Medium |
| TW-02 | | | | |

## 3. Findings
Full write-ups are in [`../findings.md`](../findings.md).

## 4. Things that needed immediate action
*List anything you reported the same day under the rules of engagement (SAP section 6), who you told, and when.*

## 5. SPRS score estimate (NIST SP 800-171 DoD Assessment Methodology)
*How the score works: every company starts at **110**. For each requirement that is **not** fully implemented, you subtract its weight (5, 3, or 1 point) from the DoD Assessment Methodology. The score can go below zero (the lowest possible is -203).*

*Use the SPRS Calculator sheet in [`../Tidewell-GRC-Workbook.xlsx`](../Tidewell-GRC-Workbook.xlsx). Look up each weight in the DoD Assessment Methodology (version 1.2.1) and record your source.*

| Item | Value |
| --- | --- |
| Starting score | 110 |
| Points subtracted (tested requirements only) | |
| Estimated score | |

**Important:** *An SPRS score can only be submitted once an SSP exists (requirement 3.12.4). Explain in one or two sentences what that means for Tidewell's February 1 deadline, and why a partial estimate must be labeled as an estimate.*

## 6. Recommendation to the risk acceptance authority
*In the federal world, this section helps the Authorizing Official decide whether to grant an Authority to Operate (ATO). At Tidewell, it's the recommendation to the CEO on whether the CUI environment's risk is acceptable as-is, acceptable with a POA&M, or not acceptable until certain fixes are made. Pick one and explain why in 3–5 sentences.*

- [ ] Acceptable as-is
- [ ] Acceptable with the POA&M, with these conditions:
- [ ] Not acceptable until these items are fixed:
