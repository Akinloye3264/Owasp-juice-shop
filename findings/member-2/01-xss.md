**Cross-Site Scripting (XSS) Testing**

**Vulnerability**
Cross-Site Scripting (XSS)

**Application**
OWASP Juice Shop

**Objective**
To test whether user-controlled input in the OWASP Juice Shop search functionality is properly sanitized before being rendered by the application.

**Test Procedure**
The application's search feature was tested using the following XSS payload:

```html
<iframe src="javascript:alert(`xss`)">
```

**Steps Performed**
1. Opened the OWASP Juice Shop application in the browser.
2. Navigated to the search functionality.
3. Entered the XSS payload into the search field.
4. Submitted the search request.
5. Observed the application's response.

**Result**
The test was successful.

The application processed the supplied payload and executed the embedded JavaScript code in the browser. An alert displaying:

```text
xss
```

was triggered.

This confirms that the tested input was not adequately sanitized or safely encoded before being rendered by the application.

Evidence
Screenshot evidence was captured showing the successful execution of the XSS payload.

**Screenshot:**

![Successful XSS Test](../../screenshots/member-2/xss-success.png)

> Replace the screenshot path above with the actual filename and location used in the repository.

## Security Impact
Successful Cross-Site Scripting vulnerabilities may allow an attacker to execute malicious JavaScript within another user's browser session.

Depending on the affected functionality and application configuration, this could potentially be used to:

 Manipulate content displayed to users.
 Redirect users to malicious pages.
 Perform actions within the application on behalf of a victim.
 Access sensitive information available to client-side scripts.
 Conduct phishing attacks within a trusted application interface.

**Root Cause**
The vulnerability occurs because user-supplied input is rendered without sufficient sanitization, validation, or output encoding.

**Recommended Mitigation**
The application should:

- Apply appropriate output encoding before displaying user-controlled input.
- Sanitize HTML input where HTML content is permitted.
- Validate input on both the client and server sides.
- Avoid dynamically inserting untrusted data into the DOM using unsafe methods.
- Implement a restrictive Content Security Policy (CSP) as an additional defensive layer.

 Conclusion
The XSS test demonstrated that specially crafted user input could trigger JavaScript execution within the OWASP Juice Shop application.

The successful alert confirms the presence of an XSS vulnerability in the tested functionality and demonstrates the security risk associated with insufficient handling of untrusted user input.
