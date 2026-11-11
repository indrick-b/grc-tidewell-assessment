# Findings — Tidewell Logistics Security Assessment

**Assessment date:** November 2, 2026
**Assessor:** Indrick Bodkin, GRC Analyst

Each finding uses the standard audit format:

- **Condition:** what I found (facts and numbers)
- **Criteria:** what the rule says should be true
- **Cause:** why the gap exists
- **Effect:** what could go wrong because of it
- **Recommendation:** what to do about it

---

## F-01: Password policy is outdated and not enforced consistently

| Field | Detail |
| --- | --- |
| Control | TW-01 |
| Frameworks | NIST CSF PR.AA-01 · NIST 800-53 IA-5(1) · NIST 800-171 3.5.7, 3.5.8 · SOC 2 CC6.1 · ISO 27001 A.5.17 · CIS 5.2 |
| Risk rating | Medium (Likelihood 4 × Impact 3 = 12) — see R-01 |
| Status | Not met |

**Condition.** Tidewell's password policy (IT-004) was written in 2016 by an IT manager who left in 2019. It has never been reviewed or approved. It requires 8-character passwords with forced complexity and a change every 90 days. The IT Manager said employees get around the rotation by adding a number to the same word (for example, "Summer2026!" then "Fall2026!"). The AD export shows 7 accounts set to never expire, including the shared `admin` account (password last set June 2019) and the CEO's account (last set April 2021).

**Criteria.** NIST SP 800-63B-4 (2025), section 3.1.1.2, says passwords used alone must be at least 15 characters (at least 8 when used with MFA). Systems must allow at least 64 characters, must not require composition rules or scheduled changes, and must check new passwords against a list of common and breached passwords. Passwords must be changed when there is evidence of compromise.

**Cause.** The policy has no owner and no review schedule.

**Effect.** Short, predictable passwords are easier to guess. Passwords that never change on admin accounts stay valid for years if they leak. The shared `admin` password is also written on a sticky note (see F-04).

**Recommendation.**
1. Replace IT-004 with a policy based on NIST SP 800-63B-4 (draft: [`password-policy-v2.md`](password-policy-v2.md)).
2. In Active Directory, set a 15-character minimum, remove the complexity requirement and the 90-day expiration, and turn on a banned-password list.
3. Remove "password never expires" from user accounts. Move service accounts to managed service accounts, or document why each one is an exception.
4. Assign the IT Manager as policy owner, with a yearly review.

**Note for the SSP:** NIST 800-171 Rev. 2 requirement 3.5.7 still uses the word "complexity." Tidewell should explain in its System Security Plan how the length and blocklist rule meets 3.5.7, and confirm that approach with Northstar.

> **Lesson learned:** A stronger password would **not** have stopped the September phishing attack, because Dana typed her real password into a fake page. MFA would have. That's why MFA (F-02) is rated higher than this finding.

---

## F-02: *(your turn)*

| Field | Detail |
| --- | --- |
| Control | |
| Frameworks | |
| Risk rating | |
| Status | |

**Condition.**

**Criteria.**

**Cause.**

**Effect.**

**Recommendation.**

---

*(Copy the F-02 block for each new finding.)*

## Controls that are working

List the controls you tested and marked **Met**, with one line of evidence each. Showing what works builds trust with leadership and auditors.

| Control | Evidence |
| --- | --- |
| | |
