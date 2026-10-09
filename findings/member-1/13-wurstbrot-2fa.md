# Solve Wurstbrot's 2FA Challenge

## Objective and result
Complete the two-factor authentication challenge for `wurstbrot`. The green success notification confirmed completion.

## Procedure
1. Log in with the challenge account using the training login flow.
2. When prompted for 2FA, configure an authenticator with the supplied training secret.
3. Enter the current six-digit TOTP code.
4. Submit the code and verify the success notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/20-wurstbrot-2fa-success.png`.

## Weakness, impact, and remediation
The challenge exposes the TOTP secret through an application data path, allowing an attacker to generate valid second factors. Protect MFA enrollment secrets, never expose them in ordinary API responses, require re-authentication for enrollment, and provide recovery controls with auditing.

## Limitation
The secret is specific to the Juice Shop training instance and must not be reused elsewhere.