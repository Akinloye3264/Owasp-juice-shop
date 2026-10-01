# Member 2 assignment

**Owner:** Enter your name.
**Scope:** 5 vulnerability sections; Score Board is shared preparation.

## Assigned sections

- [XSS](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/xss.adoc)
- [Improper Input Validation](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/improper-input-validation.adoc)
- [Broken Anti-Automation](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/broken-anti-automation.adoc)
- [Unvalidated Redirects](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/unvalidated-redirects.adoc)
- [Miscellaneous](https://github.com/Los-merengue/Walkthrough/blob/main/owasp-juice-shop/Challenges-Question/miscellaneous.adoc)

## Sections and challenges
A section is a vulnerability topic containing several individual hacking challenges. A challenge is one Score Board objective; it does not universally have sub-challenges. Some challenges have an associated coding exercise with two phases, **Find It** and **Fix It**. Hints, tutorials, and star ratings are guidance and difficulty indicators, not extra hacking challenges. Bonus objectives can appear as separate Score Board challenges.

The allocation covers all 16 topic sections, with Score Board as shared preparation. It does not establish that every challenge or coding exercise must be completed. No school brief specifying that requirement has been supplied. Each member must inventory the challenges in their sections against their running instance and record which are selected, solved, pending, or unavailable. Do not mark a whole section complete after one challenge unless the agreed assessment scope justifies that status.

[Coding challenge explanation](https://help.owasp-juice.shop/appendix/code-snippets.html) and [challenge tracking](https://help.owasp-juice.shop/part1/challenges.html).

## Source objectives to inventory

These are objective headings read from the supplied section files, not a claim that every objective is required or available in this application version. Use the running Score Board for exact names and availability.

### XSS

- [ ] Perform a persisted XSS attack without using the frontend application at all
- [ ] Use the bonus payload in the DOM XSS challenge
- [ ] Bypass the Content Security Policy and perform an XSS attack on a legacy page
- [ ] Perform a persisted XSS attack bypassing a client-side security mechanism
- [ ] Perform a DOM XSS attack
- [ ] Perform a persisted XSS attack through an HTTP header
- [ ] Perform a reflected XSS attack
- [ ] Perform a persisted XSS attack bypassing a server-side security mechanism
- [ ] Embed an XSS payload into our promo video

### Improper Input Validation

- [ ] Register as a user with administrator privileges
- [ ] Obtain a Deluxe Membership without paying for it
- [ ] Register a user with an empty email and password
- [ ] Successfully redeem an expired campaign coupon code
- [ ] Mint the Honey Pot NFT by gathering BEEs from the bee haven
- [ ] Retrieve the photo of Bjoern's cat in "melee combat-mode"
- [ ] Place an order that makes you rich
- [ ] Bypass a security control with a Poison Null Byte
- [ ] Follow the DRY principle while registering a user
- [ ] Upload a file larger than 100 kB
- [ ] Upload a file that has no .pdf or .zip extension
- [ ] Give a devastating zero-star feedback to the store

### Broken Anti-Automation

- [ ] Submit 10 or more customer feedbacks within 20 seconds
- [ ] Retrieve the language file that never made it into production
- [ ] Like any review at least three times as the same user
- [ ] Reset Morty's password via the Forgot Password mechanism

### Unvalidated Redirects

- [ ] Enforce a redirect to a page you are not supposed to redirect to
- [ ] Let us redirect you to one of our crypto currency addresses

### Miscellaneous

- [ ] Close multiple "Challenge solved"-notifications in one go
- [ ] Read our privacy policy
- [ ] Find the carefully hidden 'Score Board' page
- [ ] The Juice Shop is susceptible to a known vulnerability in a library for which an advisory has already been issued
- [ ] Behave like any "white hat" should before getting into the action
- [ ] Withdraw more ETH from the new wallet than you deposited

## Evidence and deliverables
1. Record the instance version and the selected challenge scope for every assigned section.
2. Read each objective, attempt it using the guide, and acknowledge hints or solutions used.
3. Save test-action and completion screenshots in `evidence/member-2/`.
4. Write each tested finding in `findings/member-2/`: objective, steps, observed result, captioned evidence, weakness, impact, remediation, and limitations.
5. Map tested findings to assets, trust boundaries, STRIDE threats, and controls in `assets/Threat-Model/README.md`.
6. Record unavailable or untested objectives explicitly; do not invent results.
7. Update the contribution checklist and combined report; submit work for another member to review.

Use descriptive filenames such as `challenge-name.md`, `challenge-name-action.png`, and `challenge-name-success.png`. Coding exercise completion must be recorded separately from hacking challenge completion.
