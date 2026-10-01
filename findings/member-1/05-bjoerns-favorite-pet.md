# F05 — Bjoern's Favorite Pet

**Author:** Member 1 (group lead)  
**Category:** Broken Authentication  
**Status:** Solved, confirmed by the success notification on the Forgot Password page.

## Objective
Reset the password of Bjoern's OWASP account via the Forgot Password mechanism using the truthful answer to his security question.

## Guided procedure
The supplied companion-guide procedure was followed on the local instance. The Forgot Password page at `http://localhost:3000/#/forgot-password` was used. The specific security-question answer and new password are not restated in this report.

## Result and evidence
The application showed: “You successfully solved a challenge: Bjoern's Favorite Pet (Reset the password of Bjoern's OWASP account via the Forgot Password mechanism with the original answer to his security question.)” The form also displayed “Your password was successfully changed.”

Evidence: E12 in the [evidence register](../../evidence/README.md). A Score Board card for this challenge was not captured in this screenshot.

![Bjoern's Favorite Pet success](../../evidence/member-1/12-bjoerns-favorite-pet-success.png)

**E12:** Forgot Password page with the Bjoern's Favorite Pet success banner and confirmation that the password was changed.

## Explanation and impact
The lab account used a security question whose answer can be obtained from public information. A password reset that depends only on that answer does not prove the requester controls the account. In this lab, that allowed a password change for Bjoern's OWASP identity.

## Remediation
Do not use guessable or publicly discoverable security questions as a standalone reset factor. Prefer emailed reset links with short expiry, plus MFA. Rate-limit reset attempts.

## Limitations and attribution
Only the success notification and password-changed message were captured. Score Board confirmation for this card is pending. The walkthrough was used. See [references](../../references.md).
