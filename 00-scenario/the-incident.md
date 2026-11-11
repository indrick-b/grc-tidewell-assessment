# The Incident That Started This Assessment

> Fictional scenario for a practice GRC assessment.

## What happened (September 2026)

1. **Sept 8, 2026.** Dana Ruiz, an accounts payable clerk, got an email that looked like a Microsoft 365 "password expiring" notice. She clicked the link and typed her password into a fake login page.
2. **Sept 8–15.** An attacker logged into Dana's mailbox from overseas. Her account had **no multi-factor authentication (MFA)**, so the password alone was enough. The attacker created a hidden inbox rule that moved any email containing "invoice" or "payment" into a folder Dana never checked.
3. **Sept 12.** From Dana's real mailbox, the attacker sent three customers an "updated bank details" letter. One customer paid **$48,500** to the attacker's bank account.
4. **Sept 16.** The customer called to ask why Tidewell said they hadn't been paid. Kevin Doyle (IT Manager) reset Dana's password and deleted the inbox rule.
5. **After that.** Nobody checked whether Dana's mailbox held CUI. Nobody told Northstar Defense Services. Nobody wrote down what happened. The company's incident response plan was not used.

## Why leadership is worried now

Three deadlines landed on the CEO's desk in the same month:

| From | What they want | Deadline |
| --- | --- | --- |
| Harborline Mutual (cyber insurer) | Proof of MFA, tested backups, and security training before the policy renews | January 15, 2027 |
| Northstar Defense Services (prime contractor) | Confirmation that Tidewell meets NIST SP 800-171, a System Security Plan, and an updated self-assessment score | February 1, 2027 |
| Brightwater Retail (largest customer) | Answers to a security questionnaire, and a plan to get a SOC 2 report | December 15, 2026 |

The CEO's words to the CFO: *"I don't know what we're doing right or wrong. I need someone to tell me, in plain English, what's broken, how bad it is, and what to fix first."*

## Your assignment

As Tidewell's new GRC Analyst, you will:

1. Review the evidence in [`01-evidence/`](../01-evidence/) (interview notes, policies, and system exports).
2. Test it against the control checklist in [`02-framework/`](../02-framework/).
3. Write findings, rate the risks, and build a remediation plan (POA&M).
4. Rewrite the outdated password and incident response policies.
5. Answer Brightwater's questionnaire honestly.
6. Review the vendors, run a user access review, and search the sign-in logs in Splunk.
7. Write the federal paperwork for Northstar (FIPS 199, SSP, SAP, SAR).
8. Handle the judgment calls in [`judgment-calls.md`](judgment-calls.md).
9. Brief leadership with a one-page executive summary.

Assessment date: **November 2, 2026.**
