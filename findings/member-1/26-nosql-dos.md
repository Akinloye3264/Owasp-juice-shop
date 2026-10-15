# NoSQL Denial of Service

## Objective and result

Cause the local server to sleep for a period through the designated Injection challenge. The application displayed the green NoSQL DoS success notification.

## Evidence

[45-nosql-dos-success.png](../../evidence/member-1/45-nosql-dos-success.png) shows the request result and success notification.

## Weakness and impact

Untrusted input reached an interpreted database expression capable of consuming server time. Repeated abuse could reduce availability by occupying request-processing resources.

## Remediation

Treat query input as data, use safe query APIs, allowlist expected types and operators, enforce request timeouts and resource limits, and rate-limit expensive operations.

## Limitations

This was a controlled local challenge. No sustained availability test was performed.
