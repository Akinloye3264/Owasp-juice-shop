# OWASP Juice Shop Assignment Overview

## Purpose

This repository documents a guided cybersecurity assessment of a local OWASP Juice Shop training application. The work is an educational group assignment carried out only against a deliberately vulnerable local lab. It is not a production penetration test and does not claim independent discovery of the vulnerabilities.

This overview intentionally excludes challenge answers, payloads, credentials, coupon codes, security-question answers, and step-by-step exploitation instructions.

## Source material and important links

- [Official OWASP Juice Shop repository and setup](https://github.com/juice-shop/juice-shop)
- [Official OWASP Juice Shop companion guide](https://pwning.owasp-juice.shop/)
- [Supplied assignment walkthrough](https://github.com/Los-merengue/Walkthrough/tree/main/owasp-juice-shop)
- [Supplied challenge index](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/README.adoc)
- [Supplied guided-solutions document](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenge-Solution/solutions.adoc)
- [Coding-exercise explanation](https://help.owasp-juice.shop/appendix/code-snippets.html)
- [Official challenge-tracking explanation](https://help.owasp-juice.shop/part1/challenges.html)
- [Supplied threat-model report](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/assets/Threat-Model/juiceshop_report_gpt4omini.md)

No remote URL for this group reporting repository is recorded in the local files. Its local location is `C:\Users\AKINLOYE\Documents\Owasp-juice-shop`.

## Assessment environment

- Application: OWASP Juice Shop
- Recorded version: 20.2.0
- Target: `http://localhost:3000`
- Environment: Kali Linux in Oracle VirtualBox
- Scope: the locally hosted training instance only
- Recorded assessment date: 1 October 2026
- External production systems: out of scope

Each member is expected to use their own lab instance. The Score Board is the principal source for challenge names, availability, and confirmation of completion. A response, changed application state, or attempted procedure is not by itself proof that a challenge was completed.

## Group allocation

The assignment distributes 16 vulnerability-topic sections among three members. Score Board discovery is shared preparation.

### Member 1 — six sections

- [Broken Authentication](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-authentication.adoc)
- [Broken Access Control](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-access-control.adoc)
- [Injection](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/injection.adoc)
- [Cryptographic Issues](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/cryptographic-issues.adoc)
- [Insecure Deserialization](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/insecure-deserialization.adoc)
- [Security through Obscurity](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/security-through-obscurity.adoc)

### Member 2 — five sections

- [Cross-Site Scripting (XSS)](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/xss.adoc)
- [Improper Input Validation](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/improper-input-validation.adoc)
- [Broken Anti-Automation](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-anti-automation.adoc)
- [Unvalidated Redirects](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/unvalidated-redirects.adoc)
- [Miscellaneous](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/miscellaneous.adoc)

### Member 3 — five sections

- [Sensitive Data Exposure](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/sensitive-data-exposure.adoc)
- [Observability Failures](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/observability-failures.adoc)
- [Security Misconfiguration](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/security-misconfiguration.adoc)
- [Vulnerable Components](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/vulnerable-components.adoc)
- [XML External Entities (XXE)](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/xxe.adoc)

## What counts as a task

A vulnerability section contains multiple individual hacking challenges. One Score Board objective is one challenge. Hints, tutorials, and star ratings are guidance rather than additional challenges. Some challenges also have separate coding exercises with “Find It” and “Fix It” phases; those phases must not be counted as completed unless they were separately performed and recorded.

The local files list 46 source objectives for Member 1. They do not establish that the school requires completion of all 46. The required number of challenges and whether coding exercises are included must be confirmed from the school brief.

## Working method

1. Record the Juice Shop version and selected scope.
2. Use the running Score Board to verify exact challenge names and availability.
3. Perform the selected exercise only in the local training instance.
4. Save evidence of the relevant test action and outcome.
5. Confirm completion through a success notification or green Score Board card.
6. Write a finding covering the objective, observed result, evidence, weakness, impact, remediation, and limitations.
7. Map the verified result to assets, flows, trust boundaries, STRIDE categories, and controls.
8. Update the task list, evidence register, contribution checklist, and combined report.
9. Submit the contribution for peer review before it is merged.

Walkthroughs and AI assistance may be acknowledged as guidance. Observations must still be checked against the actual local instance, and unavailable or unsuccessful objectives must be recorded honestly.

## Evidence standard

Evidence belongs in a member-specific directory such as `evidence/member-1/`. Descriptive filenames should identify the challenge and whether the image shows an action, response, or confirmed success.

Each evidence caption should state:

- what is visible;
- what the image proves;
- what it does not prove;
- whether a success notification or green Score Board card is present;
- any relevant version or environment limitation.

Attempted, unavailable, and confirmed are different statuses. A challenge must not be reported as solved solely because an action appeared to work. Screenshots intended for publication should exclude or redact real personal information, session tokens, cookies, and other secrets while preserving the original private evidence where appropriate.

## Current recorded progress

Member 1 has saved completion evidence across all six assigned sections. The current checklist contains 46 checked objectives and no unchecked objectives, with 28 detailed finding documents. Screenshots 48–62 confirm the objectives that were previously pending; Deprecated Interface in screenshot 58 is supplemental to the 46-item checklist.

The progress totals in the repository are not fully synchronized. Some summary files state 18 confirmed objectives and 16 documented findings, while the task checklist, finding directory, and newer evidence include additional work. These totals must be reconciled against the saved evidence and Score Board before submission. Unconfirmed attempts must remain distinct from confirmed completions.

Member 2 and Member 3 work is recorded as pending in the combined documentation.

## Threat-model component

The group reviews a supplied threat-model report containing a data-flow diagram, assets, processes, data stores, trust boundaries, STRIDE categories, proposed threats, and mitigations. Its scenarios are hypotheses until supported by observed lab evidence.

Each verified finding should identify:

- the affected asset or data flow;
- the relevant trust boundary;
- the applicable STRIDE interpretation;
- the evidence and its limitations;
- an appropriate defensive control.

The source threat model describes an Internet-facing system, while this assignment uses a localhost deployment. Untested phishing, denial-of-service, blockchain, or other scenarios must not be presented as completed work.

## Repository contents

- `README.md` — project summary, scope, allocation, and documentation links.
- `docs/member-1-tasks.md` — Member 1’s six sections and objective checklist.
- `docs/member-2-tasks.md` — Member 2’s five sections and objective checklist.
- `docs/member-3-tasks.md` — Member 3’s five sections and objective checklist.
- `docs/contributions.md` — responsibilities and submission checklist.
- `docs/final-report.md` — combined assessment report.
- `docs/assignment-overview.md` — this explanation of the overall assignment.
- `evidence/README.md` — evidence register and screenshot captions.
- `evidence/member-1/` — Member 1’s saved screenshots and representations.
- `findings/member-1/` — Member 1’s individual finding reports.
- `assets/Threat-Model/README.md` — threat-model review and finding mappings.
- `references.md` — sources and attribution.

## Remaining project-level work

- Replace member placeholders with actual names.
- Confirm the required challenge count and treatment of coding exercises from the school brief.
- Reconcile all progress totals with saved evidence.
- Mark each objective as selected, confirmed, attempted/unconfirmed, unavailable, or not tested.
- Complete the agreed work for all three members.
- Add missing finding reports and threat-model mappings.
- Record relevant application-version differences.
- Review evidence links and captions.
- Peer-review each contribution.
- Update the combined report and remediation priorities.
- Credit the walkthrough and AI assistance.
- Submit the project in the format required by the school.

## Important limitations

- The repository does not contain the school’s grading brief.
- Exhaustive completion of every listed objective is not established as a requirement.
- Some supplied references may contain missing files or unresolved version placeholders.
- No formal CVSS scoring was completed.
- No automated scan, production assessment, complete source-code audit, remediation implementation, or fix verification is claimed.
- Recommendations are proposed controls, not proof that fixes were implemented.

## Short explanation for another person

This assignment is a documented, guided assessment of a deliberately vulnerable local OWASP Juice Shop application. Three group members divided 16 vulnerability categories, performed selected Score Board challenges, captured evidence, explained the security weaknesses and impacts, proposed mitigations, and connected verified findings to a STRIDE-based threat model. The final submission must distinguish confirmed completions from attempts, acknowledge the walkthrough and AI assistance, and avoid claiming results that are not supported by saved evidence.
