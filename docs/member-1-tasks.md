# Member 1 assignment

**Owner:** Enter your name.
**Scope:** 6 vulnerability sections; Score Board is shared preparation.

## Assigned sections

- [Broken Authentication](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-authentication.adoc)
- [Broken Access Control](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-access-control.adoc)
- [Injection](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/injection.adoc)
- [Cryptographic Issues](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/cryptographic-issues.adoc)
- [Insecure Deserialization](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/insecure-deserialization.adoc)
- [Security through Obscurity](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/security-through-obscurity.adoc)

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

## Existing completed work

- Injection: Login Admin (F01).
- Broken Access Control: Admin Section (F02), View Basket (F04); Web3 Sandbox and five-star feedback have screenshots only.
- Broken Authentication: Password Strength (F03); Bjoern's Favorite Pet (F05).

These four findings and their eight screenshots are preserved. Other challenges within these sections remain unrecorded. Cryptographic Issues, Insecure Deserialization, and Security through Obscurity have no recorded tests yet.

## Source objectives to inventory

These are objective headings read from the supplied section files, not a claim that every objective is required or available in this application version. Use the running Score Board for exact names and availability.

### Broken Authentication

- [x] Reset the password of Bjoern's OWASP account via the Forgot Password mechanism
- [ ] Change Bender's password into slurmCl4ssic without using SQL Injection or Forgot Password
- [ ] Log in with Chris' erased user account
- [ ] Log in with Bjoern's Gmail account
- [x] Log in with the administrator's user credentials without previously changing them or applying SQL Injection
- [ ] Reset Bender's password via the Forgot Password mechanism
- [ ] Reset the password of Bjoern's internal account via the Forgot Password mechanism
- [ ] Reset Jim's password via the Forgot Password mechanism
- [ ] Solve the 2FA challenge for user "wurstbrot"

### Broken Access Control

- [ ] Reveal some behind-the-scenes information on the chatbot as a non-admin user
- [ ] Access the administration section of the store
- [ ] Change the name of a user by performing Cross-Site Request Forgery from another origin
- [ ] Find the hidden easter egg
- [ ] Get rid of all 5-star customer feedback
- [ ] Post some feedback in another user's name
- [ ] Post a product review as another user or edit any user's existing review
- [ ] Put an additional product into another user's shopping basket
- [ ] Change the href of the link within the O-Saft product description
- [ ] Request a hidden resource on server through server
- [ ] View another user's shopping basket
- [ ] Find an accidentally deployed code sandbox

### Injection

- [ ] Trick the chatbot into generating a coupon code for you
- [ ] Convince the chatbot to give you a coupon of 50% or more
- [ ] Extract the chatbot's system prompt
- [ ] Order the Christmas special offer of 2014
- [ ] Exfiltrate the entire DB schema definition via SQL Injection
- [ ] Log in with the (non-existing) accountant without ever registering that user
- [ ] Log in with the administrator's user account
- [x] Log in with Bender's user account — success banner observed in supplied chat screenshot; image file and reproduction steps pending.
- [ ] Log in with Jim's user account
- [ ] Let the server sleep for some time
- [ ] All your orders are belong to us
- [ ] Update multiple product reviews at the same time
- [ ] Infect the server with juicy malware by abusing arbitrary command execution
- [ ] Retrieve a list of all user credentials via SQL Injection

### Cryptographic Issues

- [ ] Forge a coupon code that gives you a discount of at least 80%
- [ ] Solve challenge #999
- [ ] Apply some advanced cryptanalysis to find the real easter egg
- [ ] Unlock Premium Challenge to access exclusive content
- [ ] Inform the shop about an algorithm or library it should definitely not use the way it does

### Insecure Deserialization

- [ ] Perform a Remote Code Execution that would keep a less hardened application busy forever
- [ ] Drop some explosive data into a vulnerable file-handling endpoint
- [ ] Perform a Remote Code Execution that occupies the server for a while without using infinite loops

### Security through Obscurity

- [ ] Learn about the Token Sale before its official announcement
- [ ] Prove that you actually read our privacy policy
- [ ] Rat out a notorious character hiding in plain sight in the shop

## Evidence and deliverables
1. Record the instance version and the selected challenge scope for every assigned section.
2. Read each objective, attempt it using the guide, and acknowledge hints or solutions used.
3. Save test-action and completion screenshots in `evidence/member-1/`.
4. Write each tested finding in `findings/member-1/`: objective, steps, observed result, captioned evidence, weakness, impact, remediation, and limitations.
5. Map tested findings to assets, trust boundaries, STRIDE threats, and controls in `assets/Threat-Model/README.md`.
6. Record unavailable or untested objectives explicitly; do not invent results.
7. Update the contribution checklist and combined report; submit work for another member to review.

Use descriptive filenames such as `challenge-name.md`, `challenge-name-action.png`, and `challenge-name-success.png`. Coding exercise completion must be recorded separately from hacking challenge completion.
