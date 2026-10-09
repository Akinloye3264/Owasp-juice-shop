# OWASP Juice Shop — Group Assessment Report

**Group:** BoyCode  
**Assessment date:** 1 October 2026  
**Status:** 16 Member 1 findings documented; 18 objectives confirmed and 28 of 46 listed Member 1 objectives remain unconfirmed.

## Executive summary
The group allocated all 16 vulnerability topic sections among three members to study authentication, access control, input validation, cross-site scripting, information exposure, and configuration weaknesses in a deliberately vulnerable local application. Member 1 confirmed 18 objectives across Broken Authentication, Broken Access Control, and Injection, with 16 documented findings. The remaining objectives are unconfirmed, unavailable, or not yet tested.

These results demonstrate an administrator login bypass, access to the administrator interface after compromise, authentication with a predictable administrator password, and a basket-identifier manipulation challenge. Admin Section is documented as privileged-interface access, not independent proof of a role-check bypass.

## Scope and boundaries
Testing targeted Juice Shop 20.2.0 at localhost:3000 inside Kali Linux running in Oracle VirtualBox. Each teammate is to use their own lab instance. No external production systems were included. The allocation is six sections for Member 1 and five each for Members 2 and 3; Score Board is shared orientation. Required challenge counts per section have not been established by a school brief. The project does not claim comprehensive coverage or completion of the full guide.

## Methodology
1. Install the application and establish that it loads.
2. Discover the Score Board using the provided route.
3. Follow guided challenge procedures, observe outcomes, and capture evidence.
4. Explain root causes and distinguish observations from assumptions.
5. Recommend corrective controls and peer-review the resulting reports.

The walkthrough and AI assistance were used. This is a guided learning exercise, not an independent penetration test. No remediation was implemented or retested.

## Shared preparation: Score Board discovery
The group opened `http://localhost:3000/#/score-board` to view the challenge catalogue and track progress.

![Score Board showing the discovery challenge solved](../evidence/member-1/00-score-board-discovered.png)

**Figure 1: Score Board discovery (E00).** The green Score Board card confirms completion of the shared discovery exercise. The visible challenge categories provide context for the selected assessment. This screenshot establishes the shared discovery exercise. Separate challenge evidence appears below.

## Confirmed Member 1 results
| Finding | Observation | Principal recommendation |
|---|---|---|
| [F01 Login Admin](../findings/member-1/01-login-admin.md) | Login Admin challenge completed following the supplied SQL injection input | Parameterized queries and secure password verification |
| [F02 Admin Section](../findings/member-1/02-admin-section.md) | Administrator interface accessible after admin login | Server-side role checks and correction of the login compromise |
| [F03 Password Strength](../findings/member-1/03-password-strength.md) | Existing predictable admin credential successfully used | Strong unique passwords, common-password blocking, MFA |
| [F04 View Basket](../findings/member-1/04-view-basket.md) | bid changed from 6 to 5; Score Board confirmed completion | Ownership checks on every basket request |
| Later Member 1 findings | Bender password change, erased-account login, Gmail login, password resets, 2FA, Easter Egg, Forged Feedback, and Forged Review were documented with supplied evidence | Verify password recovery, MFA, ownership, review authorship, and file-path controls server-side |

No formal CVSS scores are assigned: the session did not gather the evidence needed for a complete scoring assessment.

## Member 1 screenshot evidence

![login admin success](../evidence/member-1/01-login-admin-success.png)

**E01:** Login Admin success notification confirms challenge completion.

![admin section success](../evidence/member-1/02-admin-section-success.png)

**E02:** Administration page displays registered users, customer feedback, and the Admin Section success notification. Access was tested after administrator login.

![password strength success](../evidence/member-1/03-password-strength-success.png)

**E03:** Password Strength success notification confirms the valid-credential challenge was solved.

![view basket original](../evidence/member-1/04-view-basket-original.png)

**E04:** Original basket contains one Apple Pomace item before changing the basket identifier.

![view basket bid 6](../evidence/member-1/05-view-basket-bid-6.png)

**E05:** Firefox Session Storage shows the original basket identifier bid = 6.

![view basket bid 5](../evidence/member-1/06-view-basket-bid-5.png)

**E06:** Firefox Session Storage shows the edited basket identifier bid = 5. The displayed basket alone does not establish another user's ownership.

![member 1 all four solved](../evidence/member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

## Section allocation and remaining work

| Member | Sections | Current evidence |
|---|---|---|
| Member 1 (6 sections) | Broken Authentication; Broken Access Control; Injection; Cryptographic Issues; Insecure Deserialization; Security through Obscurity | 18 objectives confirmed; 28 of 46 listed objectives remain unconfirmed. |
| Member 2 (5 sections) | XSS; Improper Input Validation; Broken Anti-Automation; Unvalidated Redirects; Miscellaneous | Pending testing and evidence. |
| Member 3 (5 sections) | Sensitive Data Exposure; Observability Failures; Security Misconfiguration; Vulnerable Components; XXE | Pending testing and evidence. |

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

See [Member 1](member-1-tasks.md), [Member 2](member-2-tasks.md), and [Member 3](member-3-tasks.md) assignments for source objectives and deliverables.

## Remediation priorities
The [threat-model review](../assets/Threat-Model/README.md) relates observed findings to assets, trust boundaries, and threat categories in the supplied model. The source model is background analysis, not experimental evidence. Member 1 mappings are drafted; members 2 and 3 must add theirs after testing. No additional challenges are required solely to cover all source-model threats.

1. Prevent administrator authentication bypass with parameterized database access and proper credential verification.
2. Replace predictable privileged credentials and add MFA.
3. Enforce object ownership for basket access and role checks for administrative operations.
4. Add controls for the other vulnerability classes after teammates document their results.

## Limitations
- Member 1 evidence currently includes the saved screenshots listed in the evidence register. Basket API request/response evidence was not captured.
- Exact application commit, some software versions, and HTTP request/response captures were not recorded.
- The proposed normal failed-login baseline was not evidenced.
- Administrator page access was tested while authenticated as admin.
- For View Basket, returned basket contents/owner were not captured after the change; challenge completion was captured.
- No automated scan, production assessment, code audit, or fix verification was conducted.
- Teammate findings remain pending.

## Conclusion
Member 1 has confirmed 18 objectives and documented 16 findings. The remaining 28 listed objectives are unconfirmed, including the unresolved CSRF and chatbot coupon objectives and all currently untested Cryptographic Issues, Insecure Deserialization, and Security through Obscurity objectives. The group submission remains incomplete until the agreed scope is tested, documented, and peer-reviewed.

## Supporting material
[Evidence register](../evidence/README.md) · [Contributions](contributions.md) · [References](../references.md)
