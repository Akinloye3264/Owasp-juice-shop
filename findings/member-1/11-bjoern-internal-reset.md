# Reset Bjoern's Internal Account Password

## Objective and result
Reset the password of Bjoern's internal account through Forgot Password. The green success notification confirmed completion.

## Procedure
1. Open the Forgot Password page.
2. Enter `bjoern@juice-sh.op`.
3. Answer the postal-code question with `West-2082`.
4. Enter and confirm a new password.
5. Submit the form and verify the success notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/18-bjoern-internal-reset-success.png`.

## Weakness, impact, and remediation
The password reset relied on a security answer that could be derived from public biographical information. A discoverable answer is not a sufficient recovery factor. Use a single-use random reset token delivered through a verified channel, expire it quickly, rate-limit attempts, and avoid knowledge-based questions.

## Limitation
The screenshot confirms the reset challenge but does not assess the security of any real account.