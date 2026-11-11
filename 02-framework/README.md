# The Control Checklist

[`control-checklist.csv`](control-checklist.csv) lists **26 controls** to test at Tidewell. Each row is one rule in plain English, mapped to **six frameworks** so one assessment works for government and private-sector audiences. Each row also says **how** to test it.

| Framework | Who uses it | Why it's here |
| --- | --- | --- |
| **NIST Cybersecurity Framework (CSF) 2.0** | Private companies and government agencies | A common language for describing a security program to leadership |
| **NIST SP 800-53 Rev. 5** | Federal agencies and their systems (the RMF process) | The main control catalog for government GRC work |
| **NIST SP 800-171 Rev. 2** | Defense contractors handling CUI (DFARS 7012, CMMC Level 2) | Tidewell's subcontract with Northstar requires it |
| **SOC 2 Trust Services Criteria** | Service companies proving security to commercial customers | Brightwater Retail wants a SOC 2 report |
| **ISO/IEC 27001:2022 (Annex A)** | Companies worldwide, especially those with international customers | The most common international security standard |
| **CIS Controls v8.1** | Small and mid-size companies, and insurers | A practical "do these first" list that insurers often ask about |

A dash (—) means that framework has no matching requirement. The gaps are useful too: they show that frameworks overlap but aren't identical. For example, CIS Controls has nothing about background checks or physical security, and only NIST 800-171 asks for an SSP.

## How to test a control

The `test_method` column uses the three methods from NIST SP 800-53A and 800-171A:

| Method | What it means | Example at Tidewell |
| --- | --- | --- |
| **Examine** | Look at documents, settings, or records | Read the password policy; filter the AD export |
| **Interview** | Ask the people who run the control | Ask Kevin how backups are tested |
| **Test** | Make the control do something and see the result | Search the sign-in log in Splunk for logins after a termination date |

A control is stronger evidence when more than one method agrees. "Kevin said MFA is only on for six people" (interview) plus "the M365 report shows the same thing" (examine) is stronger than either alone.

For each control:

1. Follow the `test_procedure` and read the evidence in `where_to_look`.
2. Mark the status as **Met**, **Partially met**, or **Not met**.
3. Write one or two sentences of proof in `evidence_notes`. Use specific facts, such as "4 of 9 terminated users are still enabled in AD," not opinions.
4. If the status is Partially met or Not met, give it a finding ID (F-01, F-02, …) and write it up in [`03-my-work/findings.md`](../03-my-work/findings.md).

Not every control fails. Some are working, and a good assessment says so.

Before you start, read [`regulatory-applicability.md`](regulatory-applicability.md) to decide which laws and contracts actually apply to Tidewell.

> These mappings are a study aid. Check them against the official NIST, ISO, CIS, and AICPA publications before relying on them for a real assessment.
