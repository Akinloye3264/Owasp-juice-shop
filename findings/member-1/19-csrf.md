# Cross-Site Request Forgery Username Change

## Objective and status

Change the name of a user by submitting a profile request from another origin. Member 1 reports the challenge completed. The saved evidence establishes the cross-origin request, redirect response, and resulting username change. A separate green Score Board or challenge-success capture is still pending in the workspace.

## Observed procedure

1. An authenticated local training account was opened in Juice Shop.
2. A page on a different local origin submitted a profile request containing a replacement username.
3. The local Juice Shop server accepted the request and returned a redirect.
4. The profile subsequently displayed the changed username.

## Evidence

- [Profile after the request](../../evidence/member-1/23-csrf-success.png)
- [Cross-origin request](../../evidence/member-1/24-csrf-network.png)
- [Server response](../../evidence/member-1/25-csrf-response.png)

The images demonstrate the application-level effect. A new completion-indicator image should be added if available.

## Weakness and impact

The profile-changing operation accepted a state-changing request without sufficient protection against submission from another origin. A victim with an active session could have profile data changed without intending to perform that action.

## Remediation

Use anti-CSRF tokens on state-changing requests, validate the `Origin` or `Referer` where appropriate, use suitable `SameSite` cookie settings, and require re-authentication for sensitive account changes.

## Limitations

This finding applies only to the authorized local training instance. The saved files do not currently show a green Score Board card.
