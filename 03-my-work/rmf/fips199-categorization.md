# FIPS 199 Security Categorization — Tidewell CUI Environment

> Practice document. Complete each blank section.

## What this is
FIPS 199 asks three questions about a system's information. For each one, the answer is **Low**, **Moderate**, or **High**:

| Security objective | The question | Low means… | Moderate means… | High means… |
| --- | --- | --- | --- | --- |
| **Confidentiality** | How bad if the wrong people **see** it? | Limited harm | Serious harm | Severe or catastrophic harm |
| **Integrity** | How bad if someone **changes** it? | Limited | Serious | Severe or catastrophic |
| **Availability** | How bad if it's **unavailable**? | Limited | Serious | Severe or catastrophic |

**NIST SP 800-60** is the helper book. It lists common types of government information and suggests a starting level for each one. Volume II lists the types.

## Step 1: List the information types
*Find each information type in NIST SP 800-60 Vol. II and write its ID and suggested levels. Then decide whether Tidewell's situation changes the level, and explain why.*

| # | Information at Tidewell | Closest 800-60 information type (ID + name) | Suggested C / I / A | Your C / I / A | Why you changed it (or didn't) |
| --- | --- | --- | --- | --- | --- |
| 1 | Northstar shipping manifests marked CUI (item lists, quantities, pickup/delivery points, dates) | *Hint: look under Supply Chain Management* | | | *Hint: CUI Basic is protected at no less than Moderate confidentiality (32 CFR 2002.14)* |
| 2 | Customer invoices and payment records | | | | |
| 3 | Employee records (SSNs, bank accounts, via PayNest) | | | | |
| 4 | Shipment schedules in the dispatch app (APP01/SQL01, RouteLine) | | | | *Hint: what happens to Operations if dispatch is down for a day?* |

## Step 2: Apply the "high-water mark"
The system's category is the **highest** level in each column. If one information type is Moderate for confidentiality and the rest are Low, confidentiality is Moderate for the whole system.

**Security category (fill in):**

`SC Tidewell CUI Environment = {(confidentiality, ____), (integrity, ____), (availability, ____)}`

**Overall impact level:** ____ *(the highest of the three)*

## Step 3: What this means
*Two or three sentences. Which NIST SP 800-53 baseline (Low, Moderate, or High) would a federal agency select for a system at this level? Why does that matter for how much security Tidewell needs?*

## Step 4: Approval
| Role | Name | Date |
| --- | --- | --- |
| Prepared by (GRC Analyst) | Indrick Bodkin | |
| Reviewed by (System Owner) | | |
| Approved by (Authorizing Official equivalent) | | |
*Hint: at Tidewell, who would be the system owner for the CUI environment, and who has the authority to accept risk for the company?*
