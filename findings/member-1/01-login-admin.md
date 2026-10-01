# F01 — Login Admin

**Author:** Member 1 (group lead)  
**Category:** Injection — SQL injection affecting authentication  
**Status:** Solved, confirmed by the success notification and final Score Board screenshot.

## Objective
Log in as the administrator without knowing the password by testing the login input.

## Guided procedure
1. Open `http://localhost:3000/#/login`.
2. Enter the following in the email field:
   ```text
   ' OR 1=1--
   ```
3. Enter an arbitrary password and submit.
4. Observe the Login Admin success notification.

These were the supplied steps followed by a completion screenshot. The exact arbitrary password was not recorded. A normal failed-login baseline was suggested but not evidenced, so it is not claimed as performed.

## Result and evidence
The screenshot showed “You successfully solved a challenge: Login Admin”. The final Score Board also showed Login Admin in green.

Evidence: E01 and E07 in the [evidence register](../../evidence/README.md).

![login admin success](../../evidence/member-1/01-login-admin-success.png)

**E01:** Login Admin success notification confirms challenge completion.

![member 1 all four solved](../../evidence/member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

## Explanation and impact
The payload attempts to end a quoted string, add an always-true SQL condition, and comment out the remaining query. The observed administrator login is consistent with an SQL injection authentication bypass. The exact server-side query was not inspected during this test.

An attacker exploiting this lab weakness can obtain an administrator session without knowing the password. The later Admin Section exercise demonstrated access to the administration interface.

## Remediation
Use parameterized queries instead of concatenating login input into SQL. Fetch the intended account and securely verify its password hash. Apply least privilege to database access; rate limiting is supplementary and does not fix SQL injection.

## Limitations and attribution
Guided local lab test. No production system, automated password attack, database extraction, or code repair was performed. See [references](../../references.md).
