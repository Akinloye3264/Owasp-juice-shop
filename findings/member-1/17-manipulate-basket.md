# Put an Additional Product Into Another User's Basket

## Objective and result
Insert a product into another user's shopping basket. The green `Manipulate Basket` notification confirmed completion.

## Procedure
1. Capture a normal `POST /api/BasketItems` request for the authenticated user's basket.
2. Use the request editor to submit duplicate `BasketId` fields: the authenticated user's basket ID for validation and another user's basket ID for insertion.
3. Preserve the authenticated request header and product quantity.
4. Send the modified request and verify the success notification.

## Evidence
Save the supplied success screenshot as `evidence/member-1/41-basket-challenge-success.png`.

## Weakness, impact, and remediation
The server handled duplicate basket parameters inconsistently, allowing validation against the user's basket while using another basket for the write. An attacker could add products to another user's basket. Reject duplicate parameters, normalize input once, and authorize the target basket against the authenticated user before writing.

## Limitation
The screenshot proves challenge completion but does not independently identify the other basket owner's account.