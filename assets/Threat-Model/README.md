# Threat-model review and findings mapping

## Source and purpose
Review the supplied [Threat Model Report](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/assets/Threat-Model/juiceshop_report_gpt4omini.md), dated 28 September 2026. It contains an application data-flow diagram, descriptions of processes/data stores/trust boundaries, a threat table, and proposed mitigations grouped using STRIDE categories.

This file is the group's review and mapping, not a copy of that report and not a claim that the group authored its diagram. Treat the source's attack scenarios and severity labels as hypotheses to review, not evidence that each vulnerability has been tested. Its Internet-facing asset description also differs from this group's localhost lab deployment.

## What each member must do
- Member 1: Map authentication and authorization findings to affected assets and trust boundaries. Initial mapping is provided below; review it against the write-ups.
- Member 2: Add mappings for XSS and validation findings after testing. Explain how untrusted input reaches a browser execution or server validation boundary.
- Member 3: Add mappings for exposure/configuration findings after testing and compile the group's remediation priorities.
- Group lead: Include a short reviewed-model summary in the final report. Preserve source attribution; label changed assumptions and untested threats.

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
Complete this table with the remaining eight findings. Explain which model assumptions fit the observed lab, which are unverified, and which lie outside the selected 12-challenge scope. There is no need to execute every threat in the source model or add extra challenges merely to fill every STRIDE category. Do not report hypothesized phishing, denial of service, blockchain, or other untested scenarios as completed work.
