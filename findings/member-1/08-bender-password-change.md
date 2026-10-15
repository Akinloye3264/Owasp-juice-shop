# Change Bender's Password

## Objective and result
Change Bender's password to `slurmCl4ssic` without using SQL Injection or Forgot Password. The challenge success notification confirmed completion.

## Procedure
1. Obtain an authenticated Bender session.
2. Inspect the password-change request in the browser Network panel.
3. Send the password-change request without the `current` parameter, using matching `new` and `repeat` values.
4. Use Bender's bearer token in the `Authorization` header.
5. Set both password values to `slurmCl4ssic` and verify the success notification.

## Evidence
The original uncropped screenshot is saved as [15-bender-password-change-success.png](../../evidence/member-1/15-bender-password-change-success.png).

## Weakness, impact, and remediation
The endpoint accepted a password change without correctly validating the current password. An attacker with a valid session could change another account's password. Require server-side verification of the current password, use a protected POST endpoint, avoid passwords in URLs, and invalidate active sessions after a password change.

## Limitation
The screenshot proves challenge completion and shows the request parameters, but it is not a code review of the server implementation.