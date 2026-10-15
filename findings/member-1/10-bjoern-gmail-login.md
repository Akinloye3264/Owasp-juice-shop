# Log In With Bjoern's Gmail Account

## Objective and result
Log in with Bjoern's Gmail account. The successful login notification confirmed completion.

## Procedure
1. Open the Juice Shop login page.
2. Use Bjoern's Gmail address.
3. Use the Base64 value derived from the reversed email address as the password.
4. Confirm the successful login and challenge notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/17-bjoern-gmail-login-success.png`.

## Weakness, impact, and remediation
The OAuth registration flow derived a predictable password from a public email address. Anyone who knows the derivation could impersonate the account. OAuth accounts must use provider-backed authentication or random secrets and must never derive passwords from public identifiers.

## Limitation
The finding demonstrates account impersonation in the training instance only.