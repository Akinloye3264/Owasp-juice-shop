# Login Bender

## Objective and observed result
Log in with Bender's user account. The supplied chat screenshot shows Juice Shop at `http://localhost:3000/#/search` and the success banner: "You successfully solved a challenge: Login Bender (Log in with Bender's user account.)" This confirms hacking challenge completion.

## Evidence
The screenshot is visible in the conversation but is not available as a local image file. Save the original as `evidence/member-1/13-login-bender-success.png` before submission. No image file has been saved by the assistant.

Suggested caption: Local Juice Shop displays the Login Bender success notification. The screenshot confirms completion but does not show the submitted login request or payload.

## Reproduction and threat modelling
The assignment lists this objective under Injection. The actual login inputs and request have not been supplied, so the exploitation method, root cause, and remediation remain to be documented from the test evidence.

The affected asset is Bender's account and its associated private data. The relevant trust boundary is the login request crossing from the browser to the authentication service. STRIDE mapping: Spoofing through impersonation of another user; Information Disclosure if that access exposes private account data (not demonstrated by this screenshot).

## Remaining work
- Preserve the original success screenshot as the named evidence file.
- Record the exact test steps and login request, excluding session tokens from the submitted report.
- Capture the solved Login Bender card on the Score Board.
- Document the demonstrated weakness and appropriate controls once the method is confirmed.
