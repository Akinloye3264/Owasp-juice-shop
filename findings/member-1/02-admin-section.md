# F02 — Admin Section

**Author:** Member 1 (group lead)  
**Category:** Broken Access Control (challenge classification)  
**Status:** Solved, confirmed by a success notification.

## Objective
Locate and access the store's administration section.

## Guided procedure
1. Remain logged in after Login Admin.
2. Navigate to `http://localhost:3000/#/administration`.
3. Observe the administration interface and success notification.
4. Capture the page without changing records.

## Result and evidence
The page displayed Registered Users and Customer Feedback, with an Admin Section success notification. Evidence: E02 and E07 in the [evidence register](../../evidence/README.md).

![admin section success](../../evidence/member-1/02-admin-section-success.png)

**E02:** Administration page displays registered users, customer feedback, and the Admin Section success notification. Access was tested after administrator login.

![member 1 all four solved](../../evidence/member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

## Explanation and impact
This exercise demonstrates the privileged interface available after the administrator login compromise. An unlinked route is discoverable and its obscurity is not a security control.

**Access while authenticated as an administrator is not, by itself, proof of an authorization bypass.** No ordinary-user versus administrator request comparison was captured. This finding therefore documents challenge completion and the consequences of F01, rather than claiming an independently demonstrated missing authorization check.

## Remediation
Protect administrative endpoints with server-side authentication and role checks. Address the login bypass in F01. Verify that ordinary users and unauthenticated requests are rejected even when they know the route.

## Limitations and attribution
The route was supplied by the walkthrough/guidance; independent route discovery was not performed. No feedback deletion or user modification was demonstrated. See [references](../../references.md).
