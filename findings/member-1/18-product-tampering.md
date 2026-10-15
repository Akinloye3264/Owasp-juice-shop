# Product Tampering

## Objective and result
Change the hyperlink contained in the O-Saft product description so it points to a different destination. The green challenge banner confirmed completion.

## Procedure
1. Open the O-Saft product page and inspect the product description markup.
2. Identify the HTML link element in the description and locate the `href` attribute.
3. Replace the original URL with the tampered target shown in the challenge objective.
4. Save or submit the modified product content and refresh the page.
5. Confirm the success banner and the updated link target.

## Evidence
The challenge screenshot is [../../evidence/member-1/38-product-tampering-success.png](../../evidence/member-1/38-product-tampering-success.png).

![product tampering success](../../evidence/member-1/38-product-tampering-success.png)

**E38:** The screenshot shows the tampered description link was accepted and the challenge was solved.

## Weakness, impact, and remediation
The application trusted a user-controlled product description value and allowed the `href` content to be changed without suitable validation or integrity checks. An attacker could redirect users to an untrusted destination or present deceptive content inside a trusted product listing. Restrict product edits to authorized roles, validate allowed URL values, sanitize HTML, and enforce server-side integrity checks for catalog data.

## Limitation
The evidence confirms the behavior in the local training instance. It does not verify broader catalog integrity controls or the effect of similar tampering elsewhere in the application.
