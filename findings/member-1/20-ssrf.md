# Server-Side Request Forgery

## Objective and status

Request a hidden resource on the server through the server. Member 1 completed the challenge, and the supplied Score Board screenshot shows the SSRF card in green.

## Result and evidence

The local Juice Shop instance marked the SSRF challenge as solved. The green Score Board card is preserved in [39-ssrf-score-board-success.png](../../evidence/member-1/39-ssrf-score-board-success.png).

## Weakness and impact

The behavior demonstrates that server-side request functionality could be directed toward a resource that was not intended to be exposed to the user. In a non-training application, insufficient destination controls could expose internal services or data reachable by the application server.

## Remediation

Allowlist approved destinations and protocols, resolve and validate destinations before making a request, block loopback and private network ranges where they are not required, revalidate redirects, and apply network-level egress restrictions.

## Limitations

No request value or reproduction detail is recorded here because it was not preserved in the workspace. The finding is limited to the green Score Board result and does not establish access to arbitrary internal services.
