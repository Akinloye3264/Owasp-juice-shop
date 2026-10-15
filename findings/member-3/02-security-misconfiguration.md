# F3-02 — Security Misconfiguration

**Status:** Completed (5/5); evidence qualifications are stated below  
**Environment:** OWASP Juice Shop 20.2.0, `localhost:3000`, Kali Linux in VirtualBox

## Results

| Challenge | Observed result | Evidence status |
|---|---|---|
| Cross-Site Imaging | A remote image resource was accepted in the delivery-box view and the success notification was displayed. | [06-cross-site-imaging-success.png](../../evidence/member-3/06-cross-site-imaging-success.png) |
| Deprecated Interface | The obsolete B2B interface remained reachable and accepted a request after it should have been retired. | Cross-reference only: [Member 1 E52](../../evidence/member-1/58-memory-bomb-and-deprecated-interface-success.png). This file remains Member 1 evidence. |
| Error Handling | Requesting an unexpected REST path returned a verbose Express 500 response with stack information; the Score Board card is green. | [22-error-handling-success.png](../../evidence/member-3/22-error-handling-success.png) |
| Misplaced IaC Files | Infrastructure-as-Code material included in the application deliverable was publicly accessible. | [02-misplaced-iac-files-success.png](../../evidence/member-3/02-misplaced-iac-files-success.png) |
| Login Support Team | Original support-team credentials were accepted without an injection bypass. | [03-login-support-team-success.png](../../evidence/member-3/03-login-support-team-success.png) |

## Security significance

The results show several configuration and lifecycle failures: obsolete functionality remained active, infrastructure material was shipped with the application, cross-origin resources were trusted too broadly, error behavior exposed implementation detail, and a privileged support credential remained usable. Together these weaknesses increase attack surface and make reconnaissance or account compromise easier.

## Recommendations

- Remove retired routes and handlers from deployed builds; verify removal through release tests.
- Exclude IaC, backups, manifests, and internal configuration from web artifacts.
- Restrict external resource origins with an explicit allowlist and a narrowly scoped Content Security Policy.
- Return consistent generic client errors while recording detailed diagnostics only in protected logs.
- Rotate support credentials, prohibit shared accounts, require MFA, and monitor privileged logins.

## Limitations

Deprecated Interface is referenced without transferring ownership of Member 1's evidence. The other four objectives have Member 3 success captures. No production configuration review or remediation retest was performed.
