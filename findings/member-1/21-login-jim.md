# Login Jim

## Objective and status

Log in with Jim's user account. Member 1 completed the challenge using SQL injection on the login interface, and the captured screenshot confirms that the local Juice Shop instance displayed the challenge-solved banner: "You successfully solved a challenge: Login Jim (Log in with Jim's user account.)".

## Guided procedure

1. Navigate to the login page at `http://localhost:3000/#/login`.
2. In the Email field, enter the SQL injection payload:
   ```text
   jim@juice-sh.op'--
   ```
3. Enter any arbitrary value in the Password field.
4. Click the "Log in" button.
5. The backend SQL query evaluates the injected email parameter, terminates the string with the single quote `'`, and uses `--` to comment out the subsequent password evaluation clause, granting authentication as user Jim (`jim@juice-sh.op`).

## Result and evidence

The local Juice Shop instance authenticated the session and displayed the green challenge success notification.

Evidence: [40-login-jim-success.png](../../evidence/member-1/40-login-jim-success.png)

![Login Jim success](../../evidence/member-1/40-login-jim-success.png)

**E34:** The success banner confirms the Login Jim challenge was solved by authenticating as Jim via SQL injection.

## Weakness and impact

- **Weakness:** CWE-89 (Improper Neutralization of Special Elements used in an SQL Command). User input supplied to the authentication endpoint is concatenated directly into the dynamic database query without parameterization or proper sanitization.
- **Impact:** An attacker can impersonate any targeted user whose email is known or discoverable without needing their password. This enables unauthorized account takeover and access to the victim's profile and order data.

## Remediation

1. Implement parameterized queries (prepared statements) across all database authentication queries to separate SQL logic from untrusted user input.
2. Validate and sanitize user input on both the client and server side, restricting disallowed characters in authentication fields.
3. Ensure application database connections run with least-privilege permissions.

## Limitations

Conducted as a guided test in a local educational lab environment. No external network systems were affected.
