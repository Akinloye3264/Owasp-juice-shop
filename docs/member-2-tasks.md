# Member 2 — XSS and input validation

**Owner:** Enter your name.  
**Status:** Pending.  
**Scope:** Exactly four assigned challenges; Score Board is common preparation.

| Challenge | Required investigation |
|---|---|
| DOM XSS | Test the designated client-side input for DOM-based script execution; record the input and resulting behavior. |
| Reflected XSS | Follow the reflected-XSS objective and capture the affected input/request and execution evidence. |
| Zero Stars | Test whether the feedback rating restriction can be bypassed; document acceptance of a zero-star submission. |
| Repetitive Registration | Follow the challenge's password-confirmation scenario and explain the validation inconsistency. |

## Steps
1. Use your own running Juice Shop lab instance; record your version and commit.
2. Open the Score Board and complete its discovery exercise.
3. Read the relevant topic in the [supplied guide](https://github.com/Los-merengue/Walkthrough/tree/main/owasp-juice-shop/Challenges-Question).
4. Attempt each objective using hints; consult solutions when needed and acknowledge that assistance.
5. Capture a baseline where useful, the relevant test action, and completion evidence.
6. Write one report per challenge covering the objective, test steps, observed result, screenshot evidence, weakness, impact, and recommended fix.
7. Store reports in `findings/member-2/` and images in `evidence/member-2/`.
8. Add your tested findings to the threat-model mapping, identifying affected assets, trust boundaries, and controls.
9. Update your contribution entry, commit on a personal branch, and open a pull request.
10. Review one other member's reports for accurate claims and working evidence links.

## File naming
Use lowercase descriptive names, for example `dom-xss.md` and matching `-action.png` / `-success.png` images.

## Acceptance criteria
- Four reports and corresponding evidence.
- The application confirms each claimed solved challenge.
- Explanations identify the weakness, demonstrated impact, and specific remediation.
- Guidance is acknowledged and unsupported claims are excluded.
- Your files are linked from the group README when complete.

Do not duplicate Member 1's assigned challenges. If a challenge is unavailable or unexpectedly difficult, tell the lead before replacing it. No deadline was supplied here; agree a testing, writing, and review deadline with the lead.
