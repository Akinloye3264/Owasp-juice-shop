# F04 — View Basket

**Author:** Member 1 (group lead)  
**Category:** Broken Access Control — insecure direct object reference (IDOR)  
**Status:** Solved, confirmed by the final Score Board.

## Objective
View another user's shopping basket by changing the basket identifier.

## Guided procedure and observed sequence
1. Use the signed-in non-admin lab account shown in the basket screenshots.
2. Add Apple Pomace to the basket and open `http://localhost:3000/#/basket`.
3. Open Firefox Developer Tools > Storage.
4. Expand Session Storage and select `http://localhost:3000`.
5. Record the original `bid` value: `6`.
6. Edit `bid` to `5` and reload the basket page.
7. Open the Score Board and confirm View Basket is green.

## Result and evidence
The screenshots establish an original basket containing one Apple Pomace item, original session-storage bid 6, and the edited value 5. The user reported that 5 persisted after reload. The final Score Board confirmed View Basket completion.

Evidence: E04–E07 in the [evidence register](../../evidence/README.md).

A basket API request/response was suggested for troubleshooting but was not supplied. No claim is made about the exact returned contents or identity of the owner of basket 5. Persistence of bid 5 alone was not treated as proof; the final completion indicator supplied confirmation.

![view basket original](../../evidence/member-1/04-view-basket-original.png)

**E04:** Original basket contains one Apple Pomace item before changing the basket identifier.

![view basket bid 6](../../evidence/member-1/05-view-basket-bid-6.png)

**E05:** Firefox Session Storage shows the original basket identifier bid = 6.

![view basket bid 5](../../evidence/member-1/06-view-basket-bid-5.png)

**E06:** Firefox Session Storage shows the edited basket identifier bid = 5. The displayed basket alone does not establish another user's ownership.

![member 1 all four solved](../../evidence/member-1/07-member-1-all-four-solved.png)

**E07:** Final Score Board shows Login Admin, Admin Section, Password Strength, and View Basket with green solved indicators.

## Explanation and impact
The lab challenge illustrates an object-level authorization weakness: the client selects a basket identifier and the application permits access to another user's basket. Server authorization must check ownership, rather than trusting an identifier stored in the browser.

The demonstrated scope is viewing another basket. Modification, checkout, and access to all baskets were not demonstrated.

## Remediation
On every basket read or write, verify the requested basket belongs to the authenticated user, except for explicitly authorized roles. Derive ownership from the server-side authenticated identity. Unpredictable identifiers can reduce guessing but do not replace authorization.

## Limitations and attribution
Guided exercise using the supplied walkthrough's session-storage method. Exact backend implementation was not reviewed. See [references](../../references.md).
