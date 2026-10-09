# BoyCode Group Assignment — OWASP Juice Shop

A guided cybersecurity assessment of a local OWASP Juice Shop training application.

## Scope and status
The group allocation covers 16 vulnerability topic sections, divided 6/5/5. Score Board is shared preparation. The number of required challenges within each section remains subject to the assignment scope.

| Member | Sections | Current evidence |
|---|---|---|
| Member 1 (6 sections) | Broken Authentication; Broken Access Control; Injection; Cryptographic Issues; Insecure Deserialization; Security through Obscurity | 18 objectives confirmed; 28 of 46 listed objectives remain unconfirmed. Three sections have no confirmed tests. |
| Member 2 (5 sections) | XSS; Improper Input Validation; Broken Anti-Automation; Unvalidated Redirects; Miscellaneous | Pending testing and evidence. |
| Member 3 (5 sections) | Sensitive Data Exposure; Observability Failures; Security Misconfiguration; Vulnerable Components; XXE | Pending testing and evidence. |

Member 1 has 16 documented findings and 18 confirmed objectives across Broken Authentication, Broken Access Control, and Injection. Some later screenshots are evidence of attempts or unavailable behavior rather than confirmed challenge completion. The expanded six-section allocation remains in progress.

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

## Documentation
- [Combined assessment report](docs/final-report.md)
- [Member 1 assignment](docs/member-1-tasks.md)
- [Member 2 assignment](docs/member-2-tasks.md)
- [Member 3 assignment](docs/member-3-tasks.md)
- [Contribution and submission checklist](docs/contributions.md)
- [Evidence register and image captions](evidence/README.md)
- [References](references.md)
- [Threat-model review and mapping](assets/Threat-Model/README.md)

## Completed findings
See the complete [Member 1 findings directory](findings/member-1/). It includes the original four findings plus the later authentication, access-control, and review findings.

## Method and attribution
Testing took place against Juice Shop at `http://localhost:3000` inside a Kali Linux VirtualBox VM. The supplied walkthrough and AI-assisted guidance supported the tests and documentation. These are guided exercises, not claims of independent vulnerability discovery. Recommendations are proposed fixes, not implemented or verified fixes.

## Repository use
Keep application source and dependencies outside this reporting repository. Members add their own reports and screenshots on separate branches and open pull requests. Another member reviews each contribution before the lead combines the report. Replace member labels with actual names before submission.
