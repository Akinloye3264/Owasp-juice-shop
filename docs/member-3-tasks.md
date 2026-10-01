# Member 3 assignment

**Owner:** Enter your name.
**Scope:** 5 vulnerability sections; Score Board is shared preparation.

## Assigned sections

- [Sensitive Data Exposure](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/sensitive-data-exposure.adoc)
- [Observability Failures](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/observability-failures.adoc)
- [Security Misconfiguration](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/security-misconfiguration.adoc)
- [Vulnerable Components](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/vulnerable-components.adoc)
- [XXE](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/xxe.adoc)

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

## Source objectives to inventory

These are objective headings read from the supplied section files, not a claim that every objective is required or available in this application version. Use the running Score Board for exact names and availability.

### Sensitive Data Exposure

- [ ] Access a confidential document
- [ ] Perform an unwanted information disclosure by accessing data cross-domain
- [ ] A developer was careless with hardcoding unused but still valid credentials
- [ ] Access a developer's forgotten backup file
- [ ] Access a salesman's forgotten backup file
- [ ] Steal someone else's personal data without using Injection
- [ ] Inform the shop about a leaked API key
- [ ] Identify an unsafe product that was removed from the shop and inform the shop which ingredients are dangerous
- [ ] Log in with Amy's original user credentials
- [ ] Log in with the cloud admin's user account
- [ ] Log in with MC SafeSearch's original user credentials
- [ ] Determine the answer to John's security question
- [ ] Take over the wallet containing our official Soul Bound Token
- [ ] Obtain the password (hash) of the currently logged-in user directly from a REST API endpoint
- [ ] Reset Uvogin's password via the Forgot Password mechanism
- [ ] Deprive the shop of earnings by downloading the blueprint for one of its products
- [ ] Determine the answer to Emma's security question

### Observability Failures

- [ ] Gain access to any access log file of the server
- [ ] Find the endpoint that serves usage data to be scraped by a popular monitoring system
- [ ] Dumpster dive the Internet for a leaked password and log in to the original user account it belongs to
- [ ] Access a misplaced SIEM signature file.

### Security Misconfiguration

- [ ] Stick cute cross-domain kittens all over our delivery boxes
- [ ] Use a deprecated B2B interface that was not properly shut down
- [ ] Provoke an error that is neither very gracefully nor consistently handled
- [ ] Access the misplaced Infrastructure as Code files
- [ ] Log in with the support team's original user credentials

### Vulnerable Components

- [ ] Overwrite the Legal Information file
- [ ] Forge an almost properly RSA-signed JWT token
- [ ] Inform the shop about a typosquatting imposter that dug itself deep into the frontend
- [ ] Inform the shop about a typosquatting trick it has been a victim of
- [ ] Gain read access to an arbitrary local file on the web server
- [ ] Inform the development team about a danger to some of their credentials
- [ ] Forge an essentially unsigned JWT token
- [ ] Inform the shop about the use of a known vulnerable infrastructure component
- [ ] Inform the shop about a high-severity vulnerability

### XXE

- [ ] Retrieve the content of C:\Windows\system.ini or /etc/passwd from the server
- [ ] Give the server something to chew on for quite a while

## Evidence and deliverables
1. Record the instance version and the selected challenge scope for every assigned section.
2. Read each objective, attempt it using the guide, and acknowledge hints or solutions used.
3. Save test-action and completion screenshots in `evidence/member-3/`.
4. Write each tested finding in `findings/member-3/`: objective, steps, observed result, captioned evidence, weakness, impact, remediation, and limitations.
5. Map tested findings to assets, trust boundaries, STRIDE threats, and controls in `assets/Threat-Model/README.md`.
6. Record unavailable or untested objectives explicitly; do not invent results.
7. Update the contribution checklist and combined report; submit work for another member to review.

Use descriptive filenames such as `challenge-name.md`, `challenge-name-action.png`, and `challenge-name-success.png`. Coding exercise completion must be recorded separately from hacking challenge completion.

Member 3 also compiles remediation priorities from all verified group findings.
