# NoSQL Manipulation

## Objective and result

Update multiple product reviews at the same time. The local application displayed the green NoSQL Manipulation success notification.

## Evidence

[46-nosql-manipulation-success.png](../../evidence/member-1/46-nosql-manipulation-success.png) records the success notification and browser console result.

## Weakness and impact

Insufficiently constrained query input enabled a write operation to affect multiple review records rather than one authorized target. This can compromise data integrity at scale.

## Remediation

Validate identifiers and query structure, reject unexpected operators and object types, scope updates to an authorized record, and verify the affected-row count before committing changes.

## Limitations

The evidence confirms the training challenge but does not enumerate every modified record or review endpoint.
