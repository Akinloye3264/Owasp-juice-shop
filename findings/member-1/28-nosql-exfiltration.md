# NoSQL Exfiltration

## Objective and result

Complete the “All your orders are belong to us” objective. The local Juice Shop displayed the green NoSQL Exfiltration success notification while order data was returned.

## Evidence

[47-all-your-orders-success.png](../../evidence/member-1/47-all-your-orders-success.png) shows the returned order records and challenge-success notification.

## Weakness and impact

Manipulated query input allowed access to order information outside the intended record scope. Unauthorized order disclosure can expose customer purchases and transaction-related data.

## Remediation

Use safe query construction, validate input types and operators, derive customer scope from the authenticated server-side identity, and enforce object-level authorization on every returned order.

## Limitations

The finding is limited to the local training data visible in the saved evidence.
