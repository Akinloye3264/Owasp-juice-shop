# Christmas Special

## Objective and result

Order the Christmas special offer of 2014. The local Juice Shop displayed the green Christmas Special challenge-success notification, and the order summary contained the 2014 Christmas product.

## Evidence

[41-christmas-special-success.png](../../evidence/member-1/41-christmas-special-success.png) shows the success notification and completed order.

## Weakness and impact

The test demonstrated that a product not intended for the current catalogue could still be referenced and ordered. Stale or hidden records can remain security-relevant when the server accepts their identifiers without enforcing current availability.

## Remediation

Validate product availability and sale eligibility server-side when basket items are created and again during checkout. Do not rely on the user interface to hide unavailable products.

## Limitations

The screenshot confirms the challenge result in the local training instance. It does not establish the availability of other retired products.
