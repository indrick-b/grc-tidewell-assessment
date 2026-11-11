# Third-Party (Vendor) Risk Assessment

> Practice document. Evidence: [`vendor-list.csv`](../01-evidence/exports/vendor-list.csv), [`vendors/`](../01-evidence/vendors/), CFO interview, AP Clerk interview, vendor bank change log.

## Why this matters
A company can lock its own doors and still get robbed through a vendor who has a key. Bayside IT has the master key to Tidewell (Domain Admin and Global Admin). PayNest holds every employee's SSN. Checking vendors is part of checking Tidewell.

## Step 1: Tier every vendor
Score each vendor 1–3 on **data sensitivity** (what they can see) and **access level** (what they can touch). Multiply for the tier score.

| Score | Data sensitivity | Access level |
| --- | --- | --- |
| 1 | Public or low-value data | No access to Tidewell systems |
| 2 | Internal business data | Limited access (one app, read-only) |
| 3 | CUI, SSNs, bank data, or all company data | Admin access, or can move money |

| Tier score | Tier | Review depth | How often |
| --- | --- | --- | --- |
| 6–9 | **Tier 1 (Critical)** | Full questionnaire + SOC 2 or equivalent + contract review | Every year |
| 3–4 | **Tier 2 (Moderate)** | Short questionnaire + SOC 2 if available | Every 2 years |
| 1–2 | **Tier 3 (Low)** | Basic due diligence at onboarding | At renewal |

| Vendor | Data sensitivity (1–3) | Access level (1–3) | Tier score | Tier | Why |
| --- | --- | --- | --- | --- | --- |
| Bayside IT Partners | | | | | |
| PayNest Payroll | | | | | |
| Microsoft 365 | | | | | |
| RouteLine Software | | | | | |
| Dropbox (personal accounts) | | | | | *Hint: is this even a vendor? Who signed a contract?* |
| SecureShred Tampa | | | | | *Hint: check the vendor bank change log and the billing contact on the contract* |

## Step 2: Bayside IT Partners deep dive
Read [`bayside-it-questionnaire-response.md`](../01-evidence/vendors/bayside-it-questionnaire-response.md) and [`bayside-msa-excerpt.md`](../01-evidence/vendors/bayside-msa-excerpt.md).

**Red flags** *(list each one, the answer number, and why it matters. The first one is done for you)*

| # | Red flag | Evidence | Why it matters | Framework |
| --- | --- | --- | --- | --- |
| 1 | About 9 technicians share one admin account | Questionnaire Q2; `msp_tech` in Domain Admins | Tidewell can't tell which person did what, and a technician who leaves Bayside keeps the password until it's rotated (about once a year, per Q10) | 800-171 3.5.1, 3.5.2; SOC 2 CC6.1 |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

**Contract changes to ask for at renewal** *(Auto-renews January 5, 2027. Notice is due 60 days before, which is **November 6, 2026**. Check what that means for Tidewell's options today.)*

*Write the requests you'd send to the CFO and Tidewell's lawyer for the renewal negotiation. Think about: named accounts with MFA, incident notice timing (compare to DFARS 72 hours), U.S.-only access to CUI, the DFARS 7012 flow-down, right to audit, liability cap, subcontractors, and returning or deleting data at the end.*

| # | Contract request | Why |
| --- | --- | --- |
| 1 | | |

## Step 3: PayNest SOC 2 review
Read [`paynest-soc2-report-summary.md`](../01-evidence/vendors/paynest-soc2-report-summary.md).

| Question | Your answer |
| --- | --- |
| Is this a Type I or Type II? What's the difference? | |
| What period does it cover? Is there a gap between the end of that period and today? What do you ask for to cover the gap? | |
| What was the exception, and does management's response fix it? How would you confirm? | |
| What does "carved out" mean for AWS? | |
| Which **CUECs** (customer responsibilities) is Tidewell **not** doing today? Use the portal user list. | |
| Overall: accept PayNest as a vendor, accept with conditions, or escalate? | |

## Step 4: Recommendation
*Two or three sentences for the CFO: which vendor needs action first, and what action.*
