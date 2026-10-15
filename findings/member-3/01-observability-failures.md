# F3-01 — Observability Failures

**Status:** Confirmed complete (4/4)  
**Environment:** OWASP Juice Shop 20.2.0, `localhost:3000`, Kali Linux in VirtualBox

## Results

| Challenge | Observed result | Evidence |
|---|---|---|
| Access Log | A server access-log file was reachable and the application displayed the success notification. | [01-access-log-success.png](../../evidence/member-3/01-access-log-success.png) |
| Exposed Metrics | The unauthenticated metrics endpoint returned Prometheus-style application and process measurements; the success notification was displayed. | [09-exposed-metrics-success.png](../../evidence/member-3/09-exposed-metrics-success.png) |
| Leaked Access Logs | Credentials recovered from publicly exposed historical log material authenticated to the original training account. | [05-leaked-access-logs-success.png](../../evidence/member-3/05-leaked-access-logs-success.png) |
| Misplaced Signature File | A SIEM signature file stored under a publicly reachable path was retrieved and the challenge was confirmed. | [04-misplaced-signature-file-success.png](../../evidence/member-3/04-misplaced-signature-file-success.png) |

## Security significance

Operational logs, monitoring endpoints, and detection rules can disclose account identifiers, internal routes, software behavior, request volumes, and defensive logic. This information helps an attacker map the service and may expose reusable secrets. The leaked-log result also demonstrates the account-takeover consequence of retaining credentials in public artifacts.

## Recommendations

- Keep logs, SIEM rules, and monitoring endpoints outside the public web root.
- Require authenticated, network-restricted access to operational telemetry.
- Redact credentials, tokens, personal data, and sensitive query values before logging.
- Rotate any secret that appears in a log or published artifact and invalidate affected sessions.
- Apply retention limits and automated secret scanning to repositories, backups, and release packages.

## Limitations

The screenshots confirm the guided challenges on the local training instance. They do not establish exposure on a production service, exhaustively enumerate leaked data, or verify that the proposed controls have been implemented.
