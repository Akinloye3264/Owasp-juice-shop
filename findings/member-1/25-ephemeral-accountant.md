# Ephemeral Accountant

## Objective and result

Log in with the non-existing accountant account without registering that user. The local Juice Shop displayed the green Ephemeral Accountant success notification and showed an authenticated accountant identity.

## Evidence

[44-ephemeral-accountant-success.png](../../evidence/member-1/44-ephemeral-accountant-success.png) shows the authenticated state and challenge-success notification.

## Weakness and impact

The authentication flow accepted an identity that should not have existed as a registered account. Injection in authentication logic can allow impersonation and unauthorized access without valid credentials.

## Remediation

Use parameterized authentication queries, verify that the selected user is a valid active database record, securely verify password hashes, and apply server-side session validation.

## Limitations

The screenshot confirms the challenge outcome but does not represent a complete assessment of every authentication endpoint.
