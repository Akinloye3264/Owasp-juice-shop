# Threat-model review and findings mapping

## Source and purpose
Review the supplied [Threat Model Report](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/assets/Threat-Model/juiceshop_report_gpt4omini.md), dated 28 September 2026. It contains an application data-flow diagram, descriptions of processes/data stores/trust boundaries, a threat table, and proposed mitigations grouped using STRIDE categories.

This file is the group's review and mapping, not a copy of that report and not a claim that the group authored its diagram. Treat the source's attack scenarios and severity labels as hypotheses to review, not evidence that each vulnerability has been tested. Its Internet-facing asset description also differs from this group's localhost lab deployment.

## Section ownership

| Member | Sections | Current evidence |
|---|---|---|
| Member 1 (6 sections) | Broken Authentication; Broken Access Control; Injection; Cryptographic Issues; Insecure Deserialization; Security through Obscurity | All 46 listed objectives checked; 28 detailed finding reports currently present; newer results registered in evidence. |
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
| Bender Password Change | Authenticated browser request to password-change endpoint | Account takeover through missing current-password validation | Success screenshot shows the target request and challenge completion | Verify current password server-side; protect password changes; invalidate sessions |
| Chris Erased Account | Login input to user lookup and authentication process | Spoofing and access to a soft-deleted account | Success notification confirms the erased-account challenge | Parameterized queries and independent deleted-account enforcement |
| Forged Feedback | Feedback form user identifier to feedback store | Spoofing through client-controlled ownership data | Success screenshot confirms feedback under another user's identity | Derive ownership from the authenticated session |
| Forged Review | Review author field to review store | Spoofing or unauthorized modification of review ownership | Baseline and modified request screenshots plus success evidence | Derive authorship server-side and enforce review authorization |
| Bjoern/Jim Resets and Wurstbrot 2FA | Recovery and MFA flows to account authentication | Account takeover through discoverable recovery data or exposed MFA secret | Success screenshots confirm training-instance challenge completion | Random recovery tokens, rate limiting, protected MFA enrollment secrets |
| Hidden Easter Egg | Public file endpoint to hidden resource | Information disclosure through unsafe path/extension handling | Green Score Board evidence confirms the challenge | Canonicalize paths and validate the final resolved resource |
| CSRF Username Change | Cross-origin browser request to profile update process | Tampering through an unwanted authenticated state change | Saved request, response, and changed profile; updated completion-indicator capture pending | Anti-CSRF tokens, origin validation, suitable SameSite cookies, and re-authentication for sensitive changes |
| SSRF | User-controlled server-side request to a hidden server resource | Information disclosure and possible boundary crossing from the application server | Saved Score Board screenshot shows the SSRF card green | Destination allowlist, address validation, redirect revalidation, and restricted outbound access |
| Christmas Special | Product identifier through basket and checkout to catalogue/order stores | Tampering with an order by referencing an unavailable catalogue record | Success notification and completed order are saved | Enforce availability and sale eligibility during basket creation and checkout |
| Database Schema | Search input to relational database query | Information disclosure through SQL injection | Success notification and schema output are saved | Parameterized queries, least privilege, and generic errors |
| User Credentials | Search input to user database query | Information disclosure of authentication data | Success notification and returned training records are saved | Parameterized queries, least privilege, secure password hashing, and response minimization |
| Ephemeral Accountant | Login input to authentication and session processes | Spoofing a non-existing identity through injection | Success notification and authenticated accountant identity are saved | Parameterized authentication queries and validation of active persisted users |
| NoSQL DoS | Product/review query input to NoSQL processing | Denial of service through an expensive interpreted expression | Green success notification is saved; no sustained test performed | Safe query APIs, input allowlists, timeouts, resource limits, and rate limiting |
| NoSQL Manipulation | Review query/update input to review data store | Tampering affecting multiple records | Green success notification and console result are saved | Validate operators and identifiers, authorize each target, and constrain affected rows |
| NoSQL Exfiltration | Order lookup input to order data store | Information disclosure through query-scope bypass | Green success notification and returned order records are saved | Safe query construction and server-side object-level authorization |
| Chatbot objectives | User conversation to assistant tools and hidden instructions | Information disclosure and policy bypass through manipulated prompts | Success notifications for AI Debugging, Prompt Injection, Greedy Manipulation, and System Prompt Extraction | Isolate system instructions, authorize tool calls, constrain coupon generation, and treat model output as untrusted |
| Cryptographic objectives | Coupon, hidden-content, and legacy-cryptography mechanisms | Tampering or information disclosure caused by weak or reversible protection | Success notifications for Forged Coupon, #999, Nested Easter Egg, Premium Paywall, and Weird Crypto | Use modern reviewed cryptography, server-side authorization, unpredictable secrets, and integrity protection |
| Deserialization objectives | Serialized or uploaded input to server-side processing | Denial of service through unsafe parsing or execution | Success notifications for Blocked RCE DoS, Successful RCE DoS, and Memory Bomb | Avoid unsafe deserialization, validate formats, isolate processing, and enforce time and memory limits |
| Obscurity objectives | Hidden client-accessible content and metadata | Information disclosure when secrecy depends on concealment | Success notifications for Blockchain Hype, Privacy Policy Inspection, and Steganography | Enforce authorization and avoid placing secrets in client-accessible resources |
| SSTI | User-controlled template input to server execution context | Remote command execution | SSTI success notification is saved | Use non-evaluating templates, strict context escaping, sandboxing, and least privilege |
| Member 2 findings | To be documented after testing | XSS/validation mappings pending | Not yet tested by group | To be supported by results |
| Member 3 findings | To be documented after testing | Exposure/configuration mappings pending | Not yet tested by group | To be supported by results |

## Review deliverable
Extend this table with verified findings from all 16 allocated sections. Explain which model assumptions fit the observed lab, which are unverified, and which lie outside the agreed challenge scope within the 16 assigned sections. There is no need to execute every threat in the source model or add extra challenges merely to fill every STRIDE category. Do not report hypothesized phishing, denial of service, blockchain, or other untested scenarios as completed work.
