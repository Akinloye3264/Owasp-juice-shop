# F3-03 — Vulnerable Components

**Status:** Confirmed complete (9/9)  
**Environment:** OWASP Juice Shop 20.2.0, `localhost:3000`, Kali Linux in VirtualBox

## Results

| Challenge | Observed result | Evidence |
|---|---|---|
| Arbitrary File Write | The complaint upload path permitted overwriting the Legal Information file. | [20-arbitrary-file-write-success.png](../../evidence/member-3/20-arbitrary-file-write-success.png) |
| Forged Signed JWT | An almost correctly RSA-signed token was accepted for the challenge identity. | [19-forged-jwt-success.png](../../evidence/member-3/19-forged-jwt-success.png) |
| Frontend Typosquatting | The frontend dependency imposter was identified and reported. | [08-frontend-typosquatting-success.png](../../evidence/member-3/08-frontend-typosquatting-success.png) |
| Legacy Typosquatting | The historical typosquatting dependency was identified and reported. | [07-legacy-typosquatting-success.png](../../evidence/member-3/07-legacy-typosquatting-success.png) |
| Local File Read | A crafted upload-related request returned content from a local server file. | [21-local-file-read-success.png](../../evidence/member-3/21-local-file-read-success.png) |
| Supply Chain Attack | The credential-impacting dependency vulnerability was correctly reported. | [11-supply-chain-attack-success.png](../../evidence/member-3/11-supply-chain-attack-success.png) |
| Unsigned JWT | An essentially unsigned token was accepted for the designated challenge identity. | [17-unsigned-jwt-success.png](../../evidence/member-3/17-unsigned-jwt-success.png) |
| Vulnerable Infrastructure | The known-vulnerable infrastructure component was identified. | [10-vulnerable-infrastructure-success.png](../../evidence/member-3/10-vulnerable-infrastructure-success.png) |
| Vulnerable Library | A directly used dependency with a high-severity vulnerability was identified. | [12-vulnerable-library-success.png](../../evidence/member-3/12-vulnerable-library-success.png) |

## Security significance

The JWT results demonstrate authentication and identity spoofing when algorithm and key handling are not enforced. The file-read and file-write results cross the upload boundary and threaten confidentiality and integrity of server files. The dependency findings show how typosquatting, outdated components, and supply-chain weaknesses can introduce credential exposure, known exploits, or compromised code into an application.

## Recommendations

- Pin reviewed dependencies with lockfiles, verify package provenance, and scan software bills of materials in CI.
- Remove unused packages and patch or replace components with known exploitable vulnerabilities.
- Configure JWT verification with a server-selected algorithm, approved keys, issuer and audience checks, and rejection of unsigned tokens.
- Store uploads outside executable and public paths; generate server-side filenames and enforce canonical destination paths.
- Apply strict file-type, size, archive, and path validation in an isolated processing service with least filesystem privilege.
- Protect CI/CD credentials, rotate exposed secrets, and require signed, reviewed release artifacts.

## Limitations

These are guided challenge outcomes from a deliberately vulnerable local instance. Dependency identities and advisory details were submitted to the application but are not all legible in the success screenshots. No independent exploitability assessment, source-code audit, or post-remediation verification was performed.
