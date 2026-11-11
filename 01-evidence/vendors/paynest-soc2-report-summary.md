# PayNest Payroll — SOC 2 Type II Report (Summary Pages)

> Fictional report for a practice assessment. PayNest sent these summary pages on November 3, 2026, after the GRC Analyst asked for them. The full report is 84 pages and is shared under NDA.

| Item | Detail |
| --- | --- |
| Report type | SOC 2 Type II |
| Trust Services Criteria covered | Security, Availability, Confidentiality |
| Review period | April 1, 2025 – March 31, 2026 |
| Report date | June 18, 2026 |
| Auditor | Calloway & Finch CPAs (fictional) |
| Auditor's opinion | Unqualified ("the controls were suitably designed and operated effectively"), with one exception noted |
| Subservice organization | Amazon Web Services (hosting) — **carved out** (AWS controls were not tested in this report) |

## Section 4: Exception noted

**CC6.2 — Removing access for terminated PayNest employees.** The auditor sampled 25 PayNest employees who left during the review period. For **2 of 25**, access to the payroll production system was removed **6 and 11 days** after termination, instead of within PayNest's required 1 business day.

*Management's response:* "We automated the termination process in our HR system in May 2026."

## Section 3: Complementary User Entity Controls (CUECs)

PayNest's controls only work if the **customer** also does the following:

1. Customers are responsible for adding and removing their own users in the PayNest client portal.
2. Customers are responsible for turning on MFA for their client portal administrators.
3. Customers are responsible for reviewing and approving each payroll run before it is released.
4. Customers are responsible for reviewing their portal users at least once a year.
5. Customers are responsible for notifying PayNest promptly of suspected unauthorized access.

## Note from PayNest
"A bridge letter covering April 1, 2026 to today is available on request."

---

### Tidewell's PayNest client portal users (pulled by the GRC Analyst, November 3, 2026)

| Portal user | Role | MFA | Last login |
| --- | --- | --- | --- |
| pnatarajan | Portal admin | Off | 2026-10-31 |
| bramsey | Payroll processor | Off | 2026-10-30 |
| hwebb | Payroll processor | Off | 2026-10-30 |
| hreyes | Payroll viewer | Off | 2026-02-20 |
| lbrooks | HR viewer | Off | 2026-10-12 |
