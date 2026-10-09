# Log In With Chris' Erased User Account

## Objective and result
Log in with Chris' erased account. The GDPR Data Erasure success notification confirmed completion.

## Procedure
1. Open the Juice Shop login page.
2. Submit Chris' email with the SQL comment suffix and any non-empty password.
3. Confirm that authentication succeeds for the soft-deleted account.

## Evidence
Save the supplied success screenshot as `evidence/member-1/16-chris-erased-user-success.png`.

## Weakness, impact, and remediation
The login query allowed input to bypass the password and deletion-state conditions. This enabled authentication as an erased user. Use parameterized queries, enforce `deletedAt IS NULL` independently of user input, and avoid exposing SQL errors.

## Limitation
The evidence confirms the challenge result but does not establish access to every type of erased-user data.