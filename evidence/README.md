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
| E21 (saved) | [23-csrf-success.png](member-1/23-csrf-success.png) | Profile showing the username changed following the cross-origin request. Member 1 later reported the challenge complete; a new green-card or success-notification capture is still pending. |
| E22 (saved) | [24-csrf-network.png](member-1/24-csrf-network.png) | Cross-origin POST request payload containing `username=CSRF`. |
| E23 (saved) | [25-csrf-response.png](member-1/25-csrf-response.png) | Cross-origin profile request response showing the redirect and successful profile retrieval. |
| E24 (saved) | [28-hidden-easter-egg-success.png](member-1/28-hidden-easter-egg-success.png) | Score Board showing the Hidden Easter Egg challenge in green. |
| E25 (saved) | [31-forged-feedback-success.png](member-1/31-forged-feedback-success.png) | Success notification for posting feedback in another user’s name. |
| E26 (saved) | [32-review-normal-request.png](member-1/32-review-normal-request.png) | Baseline product-review request before changing the author value. |
| E27 (saved) | [33-review-forged-success.png](member-1/33-review-forged-success.png) | Success evidence for the forged product-review challenge. |
| E31 (saved) | [37-basket-challenge-success.png](member-1/37-basket-challenge-success.png) | Manipulate Basket success notification. |
| E32 (saved) | [38-product-tampering-success.png](member-1/38-product-tampering-success.png) | Product Tampering success notification. |
| E33 (saved) | [39-ssrf-score-board-success.png](member-1/39-ssrf-score-board-success.png) | Score Board showing the SSRF challenge card in green, confirming completion. |
| E34 (saved) | [40-login-jim-success.png](member-1/40-login-jim-success.png) | Login Jim success notification. |
| E35 (saved) | [41-christmas-special-success.png](member-1/41-christmas-special-success.png) | Christmas Special success notification and order summary confirm the 2014 offer was ordered. |
| E36 (saved) | [42-database-schema-success.png](member-1/42-database-schema-success.png) | Database Schema success notification with returned schema-definition data. |
| E37 (saved) | [43-user-credentials-success.png](member-1/43-user-credentials-success.png) | User Credentials success notification with returned training-account records; redact sensitive values in public copies. |
| E38 (saved) | [44-ephemeral-accountant-success.png](member-1/44-ephemeral-accountant-success.png) | Ephemeral Accountant success notification and authenticated accountant identity. |
| E39 (saved) | [45-nosql-dos-success.png](member-1/45-nosql-dos-success.png) | NoSQL DoS success notification confirms the server-sleep objective. |
| E40 (saved) | [46-nosql-manipulation-success.png](member-1/46-nosql-manipulation-success.png) | NoSQL Manipulation success notification confirms the multiple-review update objective. |
| E41 (saved) | [47-all-your-orders-success.png](member-1/47-all-your-orders-success.png) | NoSQL Exfiltration success notification with returned order data. |
| E42 (saved) | [48-privacy-policy-success.png](member-1/48-privacy-policy-success.png) | Privacy Policy Inspection success notification. |
| E43 (saved) | [49-blockchain-hype-success.png](member-1/49-blockchain-hype-success.png) | Blockchain Hype success notification and Token Sale page. |
| E44 (saved) | [50-steganography-success.png](member-1/50-steganography-success.png) | Steganography success notification. |
| E45 (saved) | [51-weird-crypto-success.png](member-1/51-weird-crypto-success.png) | Weird Crypto success notification. |
| E46 (saved) | [52-nested-easter-egg-success.png](member-1/52-nested-easter-egg-success.png) | Nested Easter Egg success notification and revealed scene. |
| E47 (saved) | [53-premium-paywall-success.png](member-1/53-premium-paywall-success.png) | Premium Paywall success notification and exclusive image. |
| E48 (saved) | [54-forged-coupon-success.png](member-1/54-forged-coupon-success.png) | Forged Coupon success notification and discounted order summary. |
| E49 (saved) | [55-challenge-999-success.png](member-1/55-challenge-999-success.png) | Imaginary Challenge success notification for challenge #999. |
| E50 (saved) | [56-blocked-rce-dos-success.png](member-1/56-blocked-rce-dos-success.png) | Blocked RCE DoS success notification. |
| E51 (saved) | [57-successful-rce-dos-success.png](member-1/57-successful-rce-dos-success.png) | Successful RCE DoS success notification. |
| E52 (saved) | [58-memory-bomb-and-deprecated-interface-success.png](member-1/58-memory-bomb-and-deprecated-interface-success.png) | Memory Bomb and supplemental Deprecated Interface success notifications. |
| E53 (saved) | [59-ai-debugging-success.png](member-1/59-ai-debugging-success.png) | AI Debugging success notification, superseding the earlier attempt-only evidence. |
| E54 (saved) | [60-chatbot-prompt-injection-and-greedy-manipulation-success.png](member-1/60-chatbot-prompt-injection-and-greedy-manipulation-success.png) | Chatbot Prompt Injection and Greedy Chatbot Manipulation success notifications. |
| E55 (saved) | [61-system-prompt-extraction-success.png](member-1/61-system-prompt-extraction-success.png) | System Prompt Extraction success notification. |
| E56 (saved) | [62-ssti-success.png](member-1/62-ssti-success.png) | SSTI success notification for the arbitrary-command-execution objective. |

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

**E21:** The profile username changed following the cross-origin request. Member 1 later reported completion, but a new green-card or success-notification capture is not yet saved in the workspace.

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

![basket challenge success](member-1/37-basket-challenge-success.png)

**E31:** The success banner confirms the basket-manipulation challenge was solved by adding a product to another user's basket.

![product tampering success](member-1/38-product-tampering-success.png)

**E32:** The success banner confirms the O-Saft product description was tampered with successfully.

![SSRF Score Board success](member-1/39-ssrf-score-board-success.png)

**E33:** The green SSRF Score Board card confirms that the hidden-resource server-side request challenge was completed.

![Christmas Special success](member-1/41-christmas-special-success.png)

**E35:** The success notification and order summary confirm that the 2014 Christmas offer was ordered.

![Database Schema success](member-1/42-database-schema-success.png)

**E36:** The success notification and returned schema content confirm completion of the Database Schema challenge.

![User Credentials success](member-1/43-user-credentials-success.png)

**E37:** The success notification confirms the User Credentials challenge. Public copies should redact the visible training credential values.

![Ephemeral Accountant success](member-1/44-ephemeral-accountant-success.png)

**E38:** The success notification and authenticated identity confirm the Ephemeral Accountant challenge.

![NoSQL DoS success](member-1/45-nosql-dos-success.png)

**E39:** The green notification confirms the server-sleep Injection challenge.

![NoSQL Manipulation success](member-1/46-nosql-manipulation-success.png)

**E40:** The green notification confirms that multiple product reviews were updated through the challenge behavior.

![NoSQL Exfiltration success](member-1/47-all-your-orders-success.png)

**E41:** The green notification and returned order records confirm the “All your orders are belong to us” objective.

![Login Jim success](member-1/40-login-jim-success.png)

**E34:** The success banner confirms the Login Jim challenge was solved by logging in with Jim's user account.

## New completion gallery

![Privacy Policy Inspection success](member-1/48-privacy-policy-success.png)

**E42:** Privacy Policy Inspection success.

![Blockchain Hype success](member-1/49-blockchain-hype-success.png)

**E43:** Blockchain Hype success.

![Steganography success](member-1/50-steganography-success.png)

**E44:** Steganography success.

![Weird Crypto success](member-1/51-weird-crypto-success.png)

**E45:** Weird Crypto success.

![Nested Easter Egg success](member-1/52-nested-easter-egg-success.png)

**E46:** Nested Easter Egg success.

![Premium Paywall success](member-1/53-premium-paywall-success.png)

**E47:** Premium Paywall success.

![Forged Coupon success](member-1/54-forged-coupon-success.png)

**E48:** Forged Coupon success with the discounted order summary.

![Challenge 999 success](member-1/55-challenge-999-success.png)

**E49:** Challenge #999 success.

![Blocked RCE DoS success](member-1/56-blocked-rce-dos-success.png)

**E50:** Blocked RCE DoS success.

![Successful RCE DoS success](member-1/57-successful-rce-dos-success.png)

**E51:** Successful RCE DoS success.

![Memory Bomb and Deprecated Interface success](member-1/58-memory-bomb-and-deprecated-interface-success.png)

**E52:** Memory Bomb and Deprecated Interface success. Deprecated Interface is supplemental to the 46-item checklist.

![AI Debugging success](member-1/59-ai-debugging-success.png)

**E53:** AI Debugging success.

![Chatbot Prompt Injection and Greedy Chatbot Manipulation success](member-1/60-chatbot-prompt-injection-and-greedy-manipulation-success.png)

**E54:** Chatbot Prompt Injection and Greedy Chatbot Manipulation success.

![System Prompt Extraction success](member-1/61-system-prompt-extraction-success.png)

**E55:** System Prompt Extraction success.

![SSTI success](member-1/62-ssti-success.png)

**E56:** SSTI success for the arbitrary-command-execution objective.

## Capture and publication checklist

### Evidence awaiting import

- Save a green Score Board or challenge-success screenshot for CSRF if available.

- Preserve readable URLs, challenge names, and success indicators.
- Prefer application-only captures; exclude unrelated chat windows.
- If publishing, redact personal email addresses and any real authentication tokens in a clearly identified redacted copy.
- Keep original screenshots unchanged where appropriate for private assessment.
- Add captions stating what an image proves and any limits.
- Each teammate uses their own evidence directory; their evidence is pending.
