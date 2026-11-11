# My Work

This folder holds my assessment of Tidewell Logistics. I completed the steps in this order:

| Step | File | What it is |
| --- | --- | --- |
| 1 | [`../02-framework/regulatory-applicability.md`](../02-framework/regulatory-applicability.md) | Decided which laws and contracts apply |
| 2 | [`rmf/fips199-categorization.md`](rmf/fips199-categorization.md) | Categorized the CUI environment (Low / Moderate / High) |
| 3 | [`rmf/security-assessment-plan.md`](rmf/security-assessment-plan.md) + [`evidence-request-list.csv`](evidence-request-list.csv) | Planned the assessment and requested evidence |
| 4 | [`Tidewell-GRC-Workbook.xlsx`](Tidewell-GRC-Workbook.xlsx) → Terminations Check | Compared HR, AD, M365, and finance-system data |
| 5 | [`splunk-investigation.md`](splunk-investigation.md) | Searched the September sign-in log in Splunk |
| 6 | [`../02-framework/control-checklist.csv`](../02-framework/control-checklist.csv) | Tested 26 controls against the evidence |
| 7 | [`user-access-review.csv`](user-access-review.csv) | Reviewed who has access to admin, finance, CUI, and payroll |
| 8 | [`vendor-risk-assessment.md`](vendor-risk-assessment.md) | Tiered vendors and reviewed Bayside and PayNest |
| 9 | [`findings.md`](findings.md) | Wrote up every gap in standard audit format |
| 10 | [`risk-register.csv`](risk-register.csv) | Rated each gap by likelihood and impact, before and after the fix |
| 11 | [`poam.csv`](poam.csv) | Built the remediation plan with owners, milestones, and dates |
| 12 | [`rmf/system-security-plan.md`](rmf/system-security-plan.md) | Wrote the SSP for Northstar |
| 13 | [`rmf/security-assessment-report.md`](rmf/security-assessment-report.md) | Reported results and estimated the SPRS score |
| 14 | [`password-policy-v2.md`](password-policy-v2.md), [`incident-response-plan-v2.md`](incident-response-plan-v2.md) | Rewrote two outdated policies |
| 15 | [`brightwater-answers.md`](brightwater-answers.md) | Answered the customer security questionnaire honestly |
| 16 | [`judgment-calls.md`](judgment-calls.md) | Handled six real-world pressure situations |
| 17 | [`stakeholder-communications.md`](stakeholder-communications.md), [`executive-summary.md`](executive-summary.md) | Explained the results to IT, leadership, and Northstar |

## Risk scoring method

**Risk score = Likelihood × Impact**, each rated 1 to 5.

| Score | Likelihood means… | Impact means… |
| --- | --- | --- |
| 1 | Very unlikely in the next year | Little or no harm |
| 2 | Unlikely | Minor cost or inconvenience |
| 3 | Possible | Noticeable cost, one customer upset, or a contract warning |
| 4 | Likely | Major cost, a lost customer, or a contract at risk |
| 5 | Almost certain, or already happening | Loss of the defense contract, insurance, or the business |

| Total score | Rating | What it means for the fix |
| --- | --- | --- |
| 15–25 | **High** | Fix within 30 days |
| 8–12 | **Medium** | Fix within 90 days |
| 1–6 | **Low** | Fix within 180 days, or accept the risk in writing |

**Inherent risk** is the risk today, before the fix. **Residual risk** is the risk left over after the planned fix. Leadership decides whether the residual risk is acceptable.

## POA&M lifecycle

`Open` → `In progress` → `Closed` (only after closure evidence is reviewed). An item can also be `Delayed` (record the new date in `milestone_changes` and keep the original date, because auditors look for slipping dates) or `Risk accepted` (only with written sign-off from the risk owner's leader).

## Working in the Excel workbook

The workbook is where the analysis happens. When a sheet is done, save it as CSV to update the matching file here, since GitHub can't preview `.xlsx` files.
