# Interview Notes — Kevin Doyle, IT Manager

**Date:** October 27, 2026 · **Interviewer:** GRC Analyst · **Length:** 55 minutes
**Purpose:** Understand how accounts, passwords, servers, patching, backups, and logging are managed.

> Fictional interview for a practice assessment.

---

**Q: How are passwords set up for employees?**
"We use the password policy from 2016. Eight characters, upper and lower case, a number, a symbol, and everyone changes it every 90 days. People complain about the 90 days, so a lot of them just add a number at the end, like Summer2026! then Fall2026!. Honestly, I'd like to change it but nobody's asked me to."

**Q: Is multi-factor authentication turned on?**
"Only for me, Andre, the CEO, the CFO, Lena in HR, and Carl. We turned it on for leadership after a conference talk last year. We never rolled it out to everyone because we were worried about the help desk calls. The VPN is password only too."

**Q: What happens when someone leaves the company?**
"HR is supposed to send us a ticket and we disable the account the same day. If we don't get a ticket, we don't know they left. I think we're pretty good about it."

**Q: Who has admin rights?**
"Me and Andre, obviously. There's also the shared `admin` account. We all know the password, and it's on a sticky note in the server closet in case of emergencies. Bayside IT has their own account. Marcus (CEO) asked for admin a few years ago and Rina in Sales needed it to install some software once. We've never really gone back and cleaned it up."

**Q: When did you last review who has access to what?**
"We haven't done a formal review. Maybe 2023? There's no schedule for it."

**Q: How do you handle patching?**
"Windows Update runs automatically on most laptops. Some people never restart, so a few are probably behind. The servers I patch on the third Tuesday of the month. FS01 is the old file server. It's on Windows Server 2012 R2 and it doesn't get updates anymore. We've been meaning to move the files off it for two years. It has all the shared drives, including the GovPrograms folder."

**Q: Are laptops encrypted?**
"New ones get BitLocker turned on. Some older ones were set up before we started doing that. I'd have to check the inventory."

**Q: Do you have antivirus or EDR?**
"Yes. Every laptop and server has our EDR agent, and Bayside watches the alerts 24/7. That one we're solid on." *(Analyst note: confirmed in the laptop inventory and the EDR console screenshot.)*

**Q: Tell me about backups.**
"Every night the file server, SQL server, and app server back up to BACKUP01. It's in the same server closet. I get an email if a job fails, but honestly those go to a folder and I don't always read them. We've never actually tried restoring from a backup. I assume it works."

**Q: How long do you keep logs? Does anyone review them?**
"Windows keeps about 30 days of security logs on the domain controller before they roll over. Nobody reviews them unless something breaks. We don't have a SIEM."

**Q: Firewall?**
"We have a business firewall at the office. Bayside reviews the rules every quarter and sends me a report. Last one was September." *(Analyst note: September 2026 firewall review report received.)*

**Q: What did you do during the September email incident?**
"I reset Dana's password, deleted the bad inbox rule, and blocked the sender. It was fixed in about an hour once we knew. I didn't look at what was in her mailbox. I didn't know I was supposed to tell anyone outside the company."
