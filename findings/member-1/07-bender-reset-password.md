# Reset Bender's Password

## Objective and observed result
Reset Bender's password via the Forgot Password mechanism using the original answer to his security question. The challenge was solved successfully on the local Juice Shop instance and the application displayed the success banner confirming completion.

## Evidence
The evidence for this challenge is preserved as a saved SVG representation of the screen: [../../evidence/member-1/14-bender-reset-success.svg](../../evidence/member-1/14-bender-reset-success.svg)

This image records the relevant state of the app: the green challenge-solved banner and the Forgot Password form showing the completed password reset flow.

## Guided procedure
1. Open the Juice Shop login page and navigate to the Forgot Password flow at `http://localhost:3000/#/forgot-password`.
2. Enter the email address for Bender: `bender@juice-sh.op`.
3. Answer the security question using the original answer: `Stop'n'Drop`.
4. Enter a new password and repeat it to confirm.
5. Submit the reset form.
6. Observe the success notification and a confirmation that the password was changed.
7. Confirm that the challenge is marked as solved on the Score Board.

## Result and impact
The application accepted the original security-answer response and allowed a password reset. This shows that a password reset mechanism based on a known or discoverable security answer can be abused if the answer is not treated as a weak factor.

## Weakness
The password-reset workflow is vulnerable when the security question answer is weak, discoverable, or publicly inferable. In this challenge, the answer could be learned from external material and used as the only reset factor.

## Remediation
- Replace low-entropy or public security questions with recovery links sent to a verified email address.
- Require short-lived reset tokens and account ownership verification.
- Add rate limiting to reset attempts and lockouts after repeated failures.
- Encourage strong, unique passwords and MFA for privileged or sensitive accounts.

## Limitations
This was a guided challenge. The report confirms the challenge outcome and the reset flow, but it does not establish that all unrelated account workflows were audited or hardened.
