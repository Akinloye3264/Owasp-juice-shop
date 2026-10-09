# Evidence register

## Availability
Member 1 evidence is saved in `evidence/member-1/`. The files below are the screenshots currently present in the repository and are linked to the corresponding findings where available.

| ID | Required filename | Caption and what it establishes |
|---|---|---|
| E00 (saved) | [00-score-board-discovered.png](member-1/00-score-board-discovered.png) | Score Board card shown green after visiting the supplied route. Shared preparation, not one of the four assigned findings. |
| E01 (saved) | [01-login-admin-success.png](member-1/01-login-admin-success.png) | Product page showing the Login Admin success notification, confirming challenge completion. |
| E02 (saved) | [02-admin-section-success.png](member-1/02-admin-section-success.png) | Administration page with Registered Users, Customer Feedback, and the Admin Section success notification. Does not establish access as an ordinary user. |
| E03 (saved) | [03-password-strength-success.png](member-1/03-password-strength-success.png) | Product page showing the Password Strength success notification, confirming the valid-credential challenge. |
| E04 (saved) | [04-view-basket-original.png](member-1/04-view-basket-original.png) | Original basket containing one Apple Pomace item. Baseline before identifier change. |
| E05 (saved) | [05-view-basket-bid-6.png](member-1/05-view-basket-bid-6.png) | Firefox Storage panel displaying the original session-storage bid value 6. |
| E06 (saved) | [06-view-basket-bid-5.png](member-1/06-view-basket-bid-5.png) | Firefox Storage panel displaying edited bid value 5. This image alone does not prove cross-user access. |
| E07 (saved) | [07-member-1-all-four-solved.png](member-1/07-member-1-all-four-solved.png) | Final Score Board showing Login Admin, Admin Section, Password Strength, and View Basket all green. Primary completion summary. |
| E12 (saved) | [12-bjoerns-favorite-pet-success.png](member-1/12-bjoerns-favorite-pet-success.png) | Forgot Password page with Bjoern's Favorite Pet success banner and “Your password was successfully changed.” Score Board card not in this shot. |
| E13 (saved) | [14-bender-reset-success.svg](member-1/14-bender-reset-success.svg) | Forgot Password page showing the successful Bender password-reset challenge banner and completion confirmation. |
| E14 (saved) | [15-bender-password-change-success.png](member-1/15-bender-password-change-success.png) | Direct password-change API request solved the Bender challenge without SQL Injection or Forgot Password. |
| E15 (saved) | [16-chris-erased-user-success.svg](member-1/16-chris-erased-user-success.svg) | Login succeeded for Chris’ erased account by bypassing the deletedAt check. |
| E16 (saved) | [17-bjoern-gmail-login-success.svg](member-1/17-bjoern-gmail-login-success.svg) | Bjoern’s Gmail OAuth account was logged into using the reversed-email and Base64-derived password. |
| E17 (saved) | [18-bjoern-internal-reset-success.png](member-1/18-bjoern-internal-reset-success.png) | Success notification for resetting Bjoern’s internal account through Forgot Password. |
| E18 (saved) | [19-jim-password-reset-success.png](member-1/19-jim-password-reset-success.png) | Success notification for resetting Jim’s password through Forgot Password. |
| E19 (saved) | [20-wurstbrot-2fa-success.png](member-1/20-wurstbrot-2fa-success.png) | Success notification for completing Wurstbrot’s 2FA challenge. |
| E20 (saved) | [21-chatbot-endpoint-unavailable.png](member-1/21-chatbot-endpoint-unavailable.png) | AI chatbot endpoint unavailable message; records an unavailable objective, not a solved challenge. |
| E21 (saved) | [23-csrf-success.png](member-1/23-csrf-success.png) | Profile showing the username changed to CSRF; the Score Board card remained gray, so completion is not established. |
| E22 (saved) | [24-csrf-network.png](member-1/24-csrf-network.png) | Cross-origin POST request payload containing `username=CSRF`. |
| E23 (saved) | [25-csrf-response.png](member-1/25-csrf-response.png) | Cross-origin profile request response showing the redirect and successful profile retrieval. |
| E24 (saved) | [28-hidden-easter-egg-success.png](member-1/28-hidden-easter-egg-success.png) | Score Board showing the Hidden Easter Egg challenge in green. |
| E25 (saved) | [31-forged-feedback-success.png](member-1/31-forged-feedback-success.png) | Success notification for posting feedback in another user’s name. |
| E26 (saved) | [32-review-normal-request.png](member-1/32-review-normal-request.png) | Baseline product-review request before changing the author value. |
| E27 (saved) | [33-review-forged-success.png](member-1/33-review-forged-success.png) | Success evidence for the forged product-review challenge. |
| E28 (saved) | [34-ai-debugging-success.png](member-1/34-ai-debugging-success.png) | Chatbot exposed its system prompt, but the AI Debugging Score Board card was not confirmed green. |
| E29 (saved) | [35-chatbot-prompt-injection-attempt.png](member-1/35-chatbot-prompt-injection-attempt.png) | Chatbot generated a 15-percent coupon attempt; the Prompt Injection card remained gray. |
| E30 (saved) | [36-chatbot-50-percent-coupon.png](member-1/36-chatbot-50-percent-coupon.png) | Chatbot generated a 50-percent-or-more coupon attempt; completion was not confirmed on the Score Board. |

## Screenshot gallery

![Score Board discovery](member-1/00-score-board-discovered.png)

**E00:** Green Score Board card confirms the shared discovery exercise.

![login admin success](member-1/01-login-admin-success.png)

**E01:** Login Admin success notification confirms challenge completion.

![admin section success](member-1/02-admin-section-success.png)

**E02:** Administration page displays registered users, customer feedback, and the Admin Section success notification. Access was tested after administrator login.

![password strength success](member-1/03-password-strength-success.png)

**E03:** Password Strength success notification confirms the valid-credential challenge was solved.

![view basket original](member-1/04-view-basket-original.png)

**E04:** Original basket contains one Apple Pomace item before changing the basket identifier.

![view basket bid 6](member-1/05-view-basket-bid-6.png)

**E05:** Firefox Session Storage shows the original basket identifier bid = 6.

![view basket bid 5](member-1/06-view-basket-bid-5.png)

**E06:** Firefox Session Storage shows the edited basket identifier bid = 5. The displayed basket alone does not establish another user's ownership.

![member 1 all four solved](member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

![Bjoern's Favorite Pet success](member-1/12-bjoerns-favorite-pet-success.png)

**E12:** Forgot Password page confirms Bjoern's Favorite Pet solved. Score Board confirmation for this card is still needed.

![Bender reset success](member-1/14-bender-reset-success.svg)

**E13:** Forgot Password page confirms the Bender password reset challenge solved. The success banner and form state show the challenge result.

![Bender password change success](member-1/15-bender-password-change-success.png)

**E14:** The password-change API request succeeded with Bender’s session token and set the password to slurmCl4ssic without using SQL Injection or Forgot Password.

![Chris erased user success](member-1/16-chris-erased-user-success.svg)

**E15:** Login succeeded for Chris’ erased user account by bypassing the deletedAt guard in the SQL login condition.

![Bjoern Gmail login success](member-1/17-bjoern-gmail-login-success.svg)

**E16:** Success banner confirms the Gmail/OAuth-derived login for Bjoern using the reversed-email Base64 password.

![Bjoern internal reset success](member-1/18-bjoern-internal-reset-success.png)

**E17:** Success banner confirms Bjoern’s internal-account password reset.

![Jim password reset success](member-1/19-jim-password-reset-success.png)

**E18:** Success banner confirms Jim’s password reset.

![Wurstbrot 2FA success](member-1/20-wurstbrot-2fa-success.png)

**E19:** Success banner confirms completion of the Wurstbrot 2FA challenge.

![Chatbot endpoint unavailable](member-1/21-chatbot-endpoint-unavailable.png)

**E20:** The AI endpoint was unavailable. This is a limitation record, not proof of challenge completion.

![CSRF profile result](member-1/23-csrf-success.png)

**E21:** The profile username changed to CSRF, but the Score Board remained gray.

![CSRF network request](member-1/24-csrf-network.png)

**E22:** Network evidence shows the cross-origin profile POST payload.

![CSRF response](member-1/25-csrf-response.png)

**E23:** Network response evidence shows the profile request redirect and follow-up response.

![Hidden Easter Egg success](member-1/28-hidden-easter-egg-success.png)

**E24:** Score Board confirms the Hidden Easter Egg challenge.

![Forged feedback success](member-1/31-forged-feedback-success.png)

**E25:** Success banner confirms feedback was posted in another user’s name.

![Normal review request](member-1/32-review-normal-request.png)

**E26:** Baseline request captured before modifying the review author.

![Forged review success](member-1/33-review-forged-success.png)

**E27:** Success evidence confirms the forged product-review challenge.

![AI debugging attempt](member-1/34-ai-debugging-success.png)

**E28:** The chatbot disclosed its system prompt, but the challenge card was not confirmed green.

![Chatbot prompt injection attempt](member-1/35-chatbot-prompt-injection-attempt.png)

**E29:** The chatbot generated a 15-percent coupon attempt; this is not confirmed challenge completion.

![Chatbot 50 percent coupon attempt](member-1/36-chatbot-50-percent-coupon.png)

**E30:** The chatbot generated a coupon stated to be worth at least 50 percent; the Score Board result remains unconfirmed.

## Capture and publication checklist
- Preserve readable URLs, challenge names, and success indicators.
- Prefer application-only captures; exclude unrelated chat windows.
- If publishing, redact personal email addresses and any real authentication tokens in a clearly identified redacted copy.
- Keep original screenshots unchanged where appropriate for private assessment.
- Add captions stating what an image proves and any limits.
- Each teammate uses their own evidence directory; their evidence is pending.
