# Find the Hidden Easter Egg

## Objective and result
Retrieve the hidden `eastere.gg` resource through the exposed file endpoint. The Score Board card turned green after the encoded path was requested.

## Procedure
1. Request the hidden resource using the encoded poison-null-byte path.
2. Keep the encoded `%2500` sequence unchanged.
3. Confirm the resource download and verify the green Score Board card.

## Evidence
Save the supplied green Score Board screenshot as `evidence/member-1/28-hidden-easter-egg-success.png`.

## Weakness, impact, and remediation
The file endpoint used an unsafe extension-validation and path-handling sequence. An attacker could bypass the intended file-type restriction and access a hidden resource. Canonicalize paths before validation, validate the final resolved file, use an allowlist of intended resources, and avoid serving sensitive files from a public directory.

## Limitation
The evidence demonstrates the challenge result but does not establish access to arbitrary server files.