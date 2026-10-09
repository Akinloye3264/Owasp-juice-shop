# Reset Jim's Password

## Objective and result
Reset Jim's password through Forgot Password. The success notification confirmed completion.

## Procedure
1. Open the Forgot Password page.
2. Enter `jim@juice-sh.op`.
3. Answer the eldest sibling's middle-name question with `Samuel`.
4. Enter and confirm a new password.
5. Submit the form and verify the success notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/19-jim-password-reset-success.png`.

## Weakness, impact, and remediation
The recovery answer was inferable from publicly available clues, allowing an attacker to reset the account password. Replace knowledge-based questions with strong, single-use recovery tokens and apply rate limiting and monitoring.

## Limitation
The result is limited to the local training account and does not prove access to unrelated accounts.