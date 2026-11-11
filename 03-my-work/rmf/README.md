# The Federal Paperwork (RMF Package)

> Practice package. Tidewell is fictional.

## What RMF is, in plain words

The **Risk Management Framework (RMF)**, from NIST SP 800-37, is the government's 7-step recipe for deciding whether a computer system is safe enough to use:

| Step | Plain words | The document it makes | Where it is here |
| --- | --- | --- | --- |
| 1. Prepare | Get organized: who's in charge, what's the plan | Roles, strategy | [`system-security-plan.md`](system-security-plan.md) section 2 |
| 2. Categorize | Decide how bad it would be if this system's data leaked, was changed, or went offline | FIPS 199 categorization | [`fips199-categorization.md`](fips199-categorization.md) |
| 3. Select | Pick the security controls that fit that category | Control baseline | [`../../02-framework/control-checklist.csv`](../../02-framework/control-checklist.csv) |
| 4. Implement | Put the controls in place and write down how | System Security Plan (SSP) | [`system-security-plan.md`](system-security-plan.md) |
| 5. Assess | Check whether the controls actually work | Security Assessment Plan (SAP) and Report (SAR) | [`security-assessment-plan.md`](security-assessment-plan.md), [`security-assessment-report.md`](security-assessment-report.md) |
| 6. Authorize | A senior leader decides whether the leftover risk is acceptable | Authorization decision (ATO) + POA&M | [`security-assessment-report.md`](security-assessment-report.md) section 6, [`../poam.csv`](../poam.csv) |
| 7. Monitor | Keep checking, and update the POA&M as things get fixed | Updated POA&M, continuous monitoring | [`../poam.csv`](../poam.csv) |

## Why a private company is doing federal paperwork

To be honest about it, a defense subcontractor like Tidewell doesn't go through the full RMF or get an ATO. Federal agencies do that for their own systems. Tidewell's rule is **NIST SP 800-171** (through DFARS 7012 and CMMC). But the paperwork is the same family:

- 800-171 requirement **3.12.4** says Tidewell must have an **SSP**.
- 800-171 requirement **3.12.2** says Tidewell must have **plans of action** (a POA&M).
- Northstar's letter asks for both by February 1, 2027.
- CUI is protected at the **moderate** confidentiality level under the CUI program rule (32 CFR Part 2002), so a FIPS 199 categorization is a useful way to show *why* the data needs protecting.

So this package does the full RMF document set on Tidewell's CUI environment. The same skills transfer directly to a federal GRC job, where you'd do this for an agency system.

**Interview line:** *"Tidewell is a contractor, so its real requirement was 800-171. I used the federal RMF document set on its CUI environment, starting with the FIPS 199 categorization, then the SSP, SAP, SAR, and POA&M. Those are the same documents I'd maintain for an agency system."*
