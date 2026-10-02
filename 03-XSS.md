# Finding 03 – Cross-Site Scripting (XSS)

**Application:**
OWASP Juice Shop

**Target:**
Local OWASP Juice Shop (localhost:3000)

**Tool Used:**
Web Browser

**Vulnerability Category:**
Cross-Site Scripting (XSS)

**Description:**
During testing, the search functionality was found to execute injected script content instead of treating the input only as normal text.

**Testing:**
A harmless XSS test payload was entered into the application's search field.

**Result:**
The application displayed a JavaScript alert popup, demonstrating that the injected content was executed.

**Security Impact:**
XSS can allow injected client-side scripts to execute in a user's browser and may affect users who interact with maliciously crafted content.

**Recommendation:**
Properly validate and encode user-supplied input before displaying it. Use context-appropriate output encoding and apply a strong Content Security Policy where appropriate.

**Evidence:**
Screenshot: 03-xss.png
