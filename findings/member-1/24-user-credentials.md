# User Credentials

## Objective and result

Retrieve the list of user credentials through SQL injection. The application displayed the green User Credentials success notification, and the saved response contained user records with credential-related values.

## Evidence

[43-user-credentials-success.png](../../evidence/member-1/43-user-credentials-success.png) confirms challenge completion. Sensitive lab values visible in the original evidence should be redacted from any public submission copy.

## Weakness and impact

SQL injection allowed unauthorized disclosure of authentication data. Exposed password hashes and account identifiers can enable offline password attacks and account compromise.

## Remediation

Use parameterized queries, restrict database privileges, store passwords using a modern adaptive password-hashing algorithm, monitor anomalous queries, and prevent sensitive fields from being returned by unrelated endpoints.

## Limitations

This result applies only to deliberately vulnerable training accounts. No real credentials were tested.
