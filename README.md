# BoyCode Group Assignment — OWASP Juice Shop

A guided cybersecurity assessment of a local OWASP Juice Shop training application.

## Scope and status
The group allocation covers 16 vulnerability topic sections, divided 6/5/5. Score Board is shared preparation. The number of required challenges within each section remains subject to the assignment scope.

| Member | Sections | Current evidence |
|---|---|---|
| Member 1 (6 sections) | Broken Authentication; Broken Access Control; Injection; Cryptographic Issues; Insecure Deserialization; Security through Obscurity | All 46 listed objectives checked; 28 detailed finding reports currently present. |
| Member 2 (5 sections) | XSS; Improper Input Validation; Broken Anti-Automation; Unvalidated Redirects; Miscellaneous | Pending testing and evidence. |
| Member 3 (selected 3 sections) | Observability Failures; Security Misconfiguration; Vulnerable Components | 18/18 source objectives completed; 22 screenshots saved, including five supplemental results; three detailed section reports added. |

Member 1 has completed all 46 listed objectives across the six assigned sections. Twenty-eight detailed finding reports are currently present, and the evidence register records the newer completions. The separate Deprecated Interface result is supplemental because it is not one of the 46 listed objectives.

Member 3 completed the selected three-section scope. Seventeen objectives have Member 3 success screenshots, while Deprecated Interface is cross-referenced to Member 1 evidence without changing ownership. Sensitive Data Exposure and XXE were reassigned.

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
See the [Member 1 findings](findings/member-1/) and [Member 3 findings](findings/member-3/) directories. Member 3's reports cover all three selected sections and record supplemental results separately.

## Method and attribution
Testing took place against Juice Shop at `http://localhost:3000` inside a Kali Linux VirtualBox VM. The supplied walkthrough and AI-assisted guidance supported the tests and documentation. These are guided exercises, not claims of independent vulnerability discovery. Recommendations are proposed fixes, not implemented or verified fixes.

## Repository use
Keep application source and dependencies outside this reporting repository. Members add their own reports and screenshots on separate branches and open pull requests. Another member reviews each contribution before the lead combines the report. Replace member labels with actual names before submission.

Group members:
[Oladipo hezekiah](https://github.com/Soft-00)[
Nelson Ojere]([url](https://github.com/rey484))
