# Post a Product Review as Another User

## Objective and result
Modify a product review so it is attributed to another user. The green `Forged Review` notification confirmed completion.

## Procedure
1. Submit a normal product review and capture the `PUT /rest/products/1/reviews` request.
2. Use the request editor to change only the author value to `admin@juice-sh.op`.
3. Resend the request and verify the success notification.

## Evidence
The success screenshot is [33-review-forged-success.png](../../evidence/member-1/33-review-forged-success.png). The baseline request is [32-review-normal-request.png](../../evidence/member-1/32-review-normal-request.png).

## Weakness, impact, and remediation
The server trusted a client-controlled author value instead of deriving review ownership from the authenticated session. An attacker could impersonate another reviewer or edit another user's review. Derive authorship server-side, reject client-supplied ownership fields, and enforce authorization for review updates.

## Limitation
The evidence demonstrates the challenge behavior in the local training instance and does not establish access to arbitrary production reviews.