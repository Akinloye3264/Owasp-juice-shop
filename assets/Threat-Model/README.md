# Threat-model review and findings mapping

## Source and purpose
Review the supplied [Threat Model Report](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/assets/Threat-Model/juiceshop_report_gpt4omini.md), dated 28 September 2026. It contains an application data-flow diagram, descriptions of processes/data stores/trust boundaries, a threat table, and proposed mitigations grouped using STRIDE categories.

This file is the group's review and mapping, not a copy of that report and not a claim that the group authored its diagram. Treat the source's attack scenarios and severity labels as hypotheses to review, not evidence that each vulnerability has been tested. Its Internet-facing asset description also differs from this group's localhost lab deployment.

## Section ownership

| Member | Sections | Current evidence |
|---|---|---|
| Member 1 (6 sections) | Broken Authentication; Broken Access Control; Injection; Cryptographic Issues; Insecure Deserialization; Security through Obscurity | Four challenges solved across three sections; three sections have no recorded tests. |
| Member 2 (5 sections) | XSS; Improper Input Validation; Broken Anti-Automation; Unvalidated Redirects; Miscellaneous | Pending testing and evidence. |
| Member 3 (5 sections) | Sensitive Data Exposure; Observability Failures; Security Misconfiguration; Vulnerable Components; XXE | Pending testing and evidence. |

Each member maps their verified findings to assets, flows, trust boundaries, threat categories, and controls. Member 3 combines remediation priorities. The lead reviews assumptions and integrates the mapping into the final report.

## Initial mapping
These are the group's analytical mappings, not quotations or exact copies of source threat rows.

| Finding | Asset or flow | Threat interpretation | Evidence and limits | Control |
|---|---|---|---|---|
| Login Admin | Browser login input to authentication process and user database | Spoofing; acquisition of administrator privileges | Challenge solved after supplied SQL injection procedure; exact SQL not captured | Parameterized queries and secure credential verification |
| Admin Section | Authenticated user to privileged administration interface | Consequence of administrator compromise | Page reached as admin; no separate role-check bypass established | Server-side role checks; fix authentication weakness |
| Password Strength | Credentials to authentication process | Spoofing using predictable administrator credentials | Existing supplied password accepted; no brute-force test performed | Unique strong credentials, MFA, common-password blocking |
| View Basket | Browser-selected basket ID to server-side basket data | Information disclosure through missing object ownership enforcement | bid 6 changed to 5 and challenge solved; returned data not captured | Ownership check on every basket request |
| Member 2 findings | To be documented after testing | XSS/validation mappings pending | Not yet tested by group | To be supported by results |
| Member 3 findings | To be documented after testing | Exposure/configuration mappings pending | Not yet tested by group | To be supported by results |

## Review deliverable
Extend this table with verified findings from all 16 allocated sections. Explain which model assumptions fit the observed lab, which are unverified, and which lie outside the agreed challenge scope within the 16 assigned sections. There is no need to execute every threat in the source model or add extra challenges merely to fill every STRIDE category. Do not report hypothesized phishing, denial of service, blockchain, or other untested scenarios as completed work.
