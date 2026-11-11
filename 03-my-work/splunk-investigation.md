# Splunk Investigation — September 2026 Sign-In and Audit Log

> Practice lab. The log is fictional. Every IP address is a reserved "documentation" address (192.0.2.x, 198.51.100.x, 203.0.113.x), so none of them belong to a real person.

## Why a GRC analyst is in Splunk
GRC analysts don't usually hunt hackers. That's the security operations team's job. But they **do** pull evidence to prove whether a control worked. Two questions in this assessment can only be answered with logs:

1. **TW-13:** Did the attacker reach CUI? If yes, Tidewell owed DoD a report within 72 hours, and it's now late.
2. **TW-14:** If someone had been reviewing logs, would they have caught the attacks?

## Set it up (no command line needed)
1. Log in to your Splunk instance (Per Scholas lab, or a free Splunk trial).
2. Go to **Settings → Add Data → Upload**.
3. Choose [`m365-signin-audit-log-sep-2026.csv`](../01-evidence/exports/m365-signin-audit-log-sep-2026.csv).
4. Source type: **csv**. Splunk should read the time from the `_time` column. Check that the events show September 2026 dates.
5. Index: **main** (or make one called `tidewell`). Click **Review**, then **Submit**, then **Start Searching**.

## Search building blocks
These are the basic SPL (Search Processing Language) pieces from the Splunk Core User course. Put them together yourself to answer the questions.

| What you want | SPL piece |
| --- | --- |
| Start with the data | `index=main source="m365-signin-audit-log-sep-2026.csv"` |
| Keep only some events | `country!="US"` or `operation="New-InboxRule"` |
| Count things | `\| stats count by user` |
| Count with more than one column | `\| stats count by user, country` |
| See first and last times | `\| stats min(_time) as first max(_time) as last by user` then `\| convert ctime(first) ctime(last)` |
| Show a clean table | `\| table _time user operation client_ip country details` |
| Sort | `\| sort _time` |
| Find words inside a field | `details="*CUI*"` |

## Questions to answer
Write your answer, the search you used, and a screenshot file name for each. Screenshots are your evidence, so save them in `03-my-work/screenshots/`.

| # | Question | Your answer | Your search | Screenshot |
| --- | --- | --- | --- | --- |
| 1 | Which account(s) signed in from outside the U.S.? From where, and for how many days? | | | |
| 2 | What exact time did the first foreign sign-in happen? How long until IT acted? | | | |
| 3 | What did the attacker do in the first 10 minutes? Describe the inbox rule in plain words. | | | |
| 4 | **Did the attacker open any email that held CUI?** List the subjects and times. | | | |
| 5 | Who received emails sent by the attacker? | | | |
| 6 | Did any **terminated** employee sign in during September? Compare with the HR terminations list. What did they do? | | | |
| 7 | What happened on September 24 between 2:00 and 2:30 a.m.? How many accounts were targeted? Did any attempt succeed? Was anyone alerted? | | | |
| 8 | Why didn't MFA show up on the attacker's sign-ins? Use the `mfa_result` field. | | | |

## What it means (fill this in after the questions)
*For each question that found a problem, which control and finding does it support? Does question 4 change what Tidewell must do about the DFARS 72-hour rule? Does question 6 need same-day escalation under the SAP rules of engagement?*

**Interview line:** *"I loaded a month of sign-in logs into Splunk and used stats and table searches to prove whether the controls worked. One search showed the attacker opened emails with CUI attachments, which turned a fraud incident into a DFARS reporting obligation."* (Say this only after you've done it yourself.)
