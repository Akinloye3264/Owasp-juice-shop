# Post Feedback in Another User's Name

## Objective and result
Submit customer feedback while assigning it to another user's account. The green `Forged Feedback` notification confirmed completion.

## Procedure
1. Open the Contact Us feedback form while logged in as a normal user.
2. Inspect the form and remove the `hidden` attribute from the `userId` input.
3. Enter another user's identifier, complete the comment, rating, and CAPTCHA fields, and submit.
4. Confirm the challenge success notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/31-forged-feedback-success.png`.

## Weakness, impact, and remediation
The server trusted a client-controlled user identifier instead of deriving the author from the authenticated session. An attacker could submit feedback under another user's identity. Ignore client-supplied ownership fields, derive the author from the verified session, and enforce authorization server-side.

## Limitation
The evidence proves the challenge result in the local training instance but does not assess other feedback or account operations.