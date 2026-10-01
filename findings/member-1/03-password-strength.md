# F03 — Password Strength

**Author:** Member 1 (group lead)  
**Category:** Broken Authentication  
**Status:** Solved, confirmed by a success notification.

## Objective
Authenticate using the administrator's existing credentials without SQL injection or changing the password.

## Guided procedure
1. Log out of the current session.
2. Open `http://localhost:3000/#/login`.
3. Enter the lab credentials supplied in the guidance:
   - Email: `admin@juice-sh.op`
   - Password: `admin123`
4. Submit the login form and capture the Password Strength success notification.

## Result and evidence
The screenshot explicitly confirmed Password Strength completion. Evidence: E03 and E07 in the [evidence register](../../evidence/README.md).

![password strength success](../../evidence/member-1/03-password-strength-success.png)

**E03:** Password Strength success notification confirms the valid-credential challenge was solved.

![member 1 all four solved](../../evidence/member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

## Explanation and impact
A common, predictable administrator password allows normal authentication by someone who knows or guesses it. Unlike F01, this test uses a valid password and does not alter SQL query logic. The credential was supplied by guidance, not independently cracked or discovered through a dictionary attack.

The successful administrator login demonstrates compromise of a privileged lab account. No rate-limit or lockout behavior was tested.

## Remediation
Replace predictable/default passwords, reject common or compromised passwords, and require strong unique administrator credentials. Add MFA and appropriate login throttling and monitoring.

## Limitations and attribution
Only the supplied credential was demonstrated; no brute-force campaign or password reset was performed. These are deliberately vulnerable lab credentials. See [references](../../references.md).
