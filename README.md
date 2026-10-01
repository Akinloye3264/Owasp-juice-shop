# BoyCode Group Assignment — OWASP Juice Shop

A guided cybersecurity assessment of a local OWASP Juice Shop training application.

## Scope and status
The group lead selected 12 distinct challenges from the supplied walkthrough, four per member. Score Board is shared preparation. This is a selected lab assessment, not a claim to have completed the entire walkthrough. No separate marking rubric was supplied.

**Member 1's four practical challenges are confirmed solved in screenshots shown during the session. Members 2 and 3 are pending.** All eight Member 1 evidence screenshots are saved, captioned, and embedded in the report and corresponding findings.

| Owner | Challenges | Status |
|---|---|---|
| Member 1 — group lead | Login Admin; Admin Section; Password Strength; View Basket | Practical work complete |
| Member 2 | DOM XSS; Reflected XSS; Zero Stars; Repetitive Registration | Pending |
| Member 3 | Confidential Document; Exposed Metrics; Error Handling; Forgotten Developer Backup | Pending |

## Documentation
- [Combined assessment report](docs/final-report.md)
- [Member 2 assignment](docs/member-2-tasks.md)
- [Member 3 assignment](docs/member-3-tasks.md)
- [Contribution and submission checklist](docs/contributions.md)
- [Evidence register and image captions](evidence/README.md)
- [References](references.md)
- [Threat-model review and mapping](assets/Threat-Model/README.md)

## Completed findings
1. [Login Admin](findings/member-1/01-login-admin.md)
2. [Admin Section](findings/member-1/02-admin-section.md)
3. [Password Strength](findings/member-1/03-password-strength.md)
4. [View Basket](findings/member-1/04-view-basket.md)

## Method and attribution
Testing took place against Juice Shop at `http://localhost:3000` inside a Kali Linux VirtualBox VM. The supplied walkthrough and AI-assisted guidance supported the tests and documentation. These are guided exercises, not claims of independent vulnerability discovery. Recommendations are proposed fixes, not implemented or verified fixes.

## Repository use
Keep application source and dependencies outside this reporting repository. Members add their own reports and screenshots on separate branches and open pull requests. Another member reviews each contribution before the lead combines the report. Replace member labels with actual names before submission.
