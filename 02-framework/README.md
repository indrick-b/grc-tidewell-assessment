# The Control Checklist

[`control-checklist.csv`](control-checklist.csv) lists 23 controls to test at Tidewell. Each row is one rule written in plain English, mapped to four frameworks so the same assessment works for government and private-sector audiences.

| Framework | Who uses it | Why it's here |
| --- | --- | --- |
| **NIST Cybersecurity Framework (CSF) 2.0** | Private companies and government agencies | A common language for describing a security program to leadership |
| **NIST SP 800-53 Rev. 5** | Federal agencies and their systems (the RMF process) | The main control catalog for government GRC work |
| **NIST SP 800-171 Rev. 2** | Defense contractors handling CUI (DFARS 7012, CMMC Level 2) | Tidewell's subcontract with Northstar requires it |
| **SOC 2 Trust Services Criteria** | Service companies proving security to commercial customers | Brightwater Retail wants a SOC 2 report |

A dash (—) means that framework has no matching requirement. The gaps are useful too: they show that frameworks overlap but aren't identical.

## How to use it

For each control:

1. Read the evidence listed under `where_to_look`.
2. Mark the status as **Met**, **Partially met**, or **Not met**.
3. Write one or two sentences of proof in `evidence_notes`. Use specific facts, such as "4 of 9 terminated users are still enabled in AD," not opinions.
4. If the status is Partially met or Not met, give it a finding ID (F-01, F-02, …) and write it up in [`03-my-work/findings.md`](../03-my-work/findings.md).

Not every control fails. Some are working, and a good assessment says so.

> These mappings are a study aid. Check them against the official NIST and AICPA publications before relying on them for a real assessment.
