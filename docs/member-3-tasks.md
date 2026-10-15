# Member 3 assignment

**Owner:** Member 3
**Completed scope:** Observability Failures, Security Misconfiguration, and Vulnerable Components (18 source objectives).

Sensitive Data Exposure and XXE were reassigned and are not claimed as Member 3 work in this checklist.

## Assigned sections

- [Observability Failures](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/observability-failures.adoc)
- [Security Misconfiguration](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/security-misconfiguration.adoc)
- [Vulnerable Components](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/vulnerable-components.adoc)

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

## Source objectives to inventory

These are objective headings read from the supplied section files, not a claim that every objective is required or available in this application version. Use the running Score Board for exact names and availability.

### Observability Failures

- [x] Gain access to any access log file of the server
- [x] Find the endpoint that serves usage data to be scraped by a popular monitoring system
- [x] Dumpster dive the Internet for a leaked password and log in to the original user account it belongs to
- [x] Access a misplaced SIEM signature file.

### Security Misconfiguration

- [x] Stick cute cross-domain kittens all over our delivery boxes
- [x] Use a deprecated B2B interface that was not properly shut down — completion is cross-referenced to Member 1 evidence E52; it is not relabeled as Member 3 evidence
- [x] Provoke an error that is neither very gracefully nor consistently handled
- [x] Access the misplaced Infrastructure as Code files
- [x] Log in with the support team's original user credentials

### Vulnerable Components

- [x] Overwrite the Legal Information file
- [x] Forge an almost properly RSA-signed JWT token
- [x] Inform the shop about a typosquatting imposter that dug itself deep into the frontend
- [x] Inform the shop about a typosquatting trick it has been a victim of
- [x] Gain read access to an arbitrary local file on the web server
- [x] Inform the development team about a danger to some of their credentials
- [x] Forge an essentially unsigned JWT token
- [x] Inform the shop about the use of a known vulnerable infrastructure component
- [x] Inform the shop about a high-severity vulnerability

## Completion summary

| Section | Completed | Evidence note |
|---|---:|---|
| Observability Failures | 4/4 | Four Member 3 success screenshots |
| Security Misconfiguration | 5/5 | Four Member 3 success screenshots and one Member 1 cross-reference |
| Vulnerable Components | 9/9 | Nine Member 3 success screenshots |
| **Total** | **18/18** | **Member 3's selected three-section scope is complete** |

Five additional Member 3 screenshots record supplemental challenges outside this 18-objective scope: Security Policy, Security Advisory, Forgotten Developer Backup, Forgotten Sales Backup, and Upload Type. The Member 3 evidence directory now contains 22 screenshots in total.

## Evidence and deliverables
1. Record the instance version and the selected challenge scope for every assigned section.
2. Read each objective, attempt it using the guide, and acknowledge hints or solutions used.
3. Save test-action and completion screenshots in `evidence/member-3/`.
4. Write each tested finding in `findings/member-3/`: objective, steps, observed result, captioned evidence, weakness, impact, remediation, and limitations.
5. Map tested findings to assets, trust boundaries, STRIDE threats, and controls in `assets/Threat-Model/README.md`.
6. Record unavailable or untested objectives explicitly; do not invent results.
7. Update the contribution checklist and combined report; submit work for another member to review.

Use descriptive filenames such as `challenge-name.md`, `challenge-name-action.png`, and `challenge-name-success.png`. Coding exercise completion must be recorded separately from hacking challenge completion.

Member 3 also compiles remediation priorities from all verified group findings. See the [Member 3 findings index](../findings/member-3/README.md).
