# Database Schema

## Objective and result

Exfiltrate the database schema definition through SQL injection. The local application displayed the green Database Schema success notification, while the adjacent response showed schema-definition content.

## Evidence

[42-database-schema-success.png](../../evidence/member-1/42-database-schema-success.png) records the challenge notification and returned schema data.

## Weakness and impact

Database input was interpreted as query syntax, enabling disclosure of structural metadata. Schema information can help an attacker identify sensitive tables, columns, and relationships for further attacks.

## Remediation

Use parameterized queries for all user-controlled values, avoid dynamic query construction, apply least-privilege database permissions, and return generic error responses.

## Limitations

The finding documents the saved challenge result only. It is not a complete review of every query or database permission.
