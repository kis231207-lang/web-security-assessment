# Finding 04 – Sensitive Data Exposure

**Application:**
OWASP Juice Shop

**Target:**
Local OWASP Juice Shop (localhost:3000)

**Tool Used:**
Web Browser

**Vulnerability Category:**
Sensitive Data Exposure / Information Disclosure

**Description:**
During testing, the application's `/ftp` directory was found to be publicly accessible and exposed files that contained sensitive or confidential information.

**Testing:**
The following path was accessed:

`/ftp`

The directory listing included a file named `acquisitions.md`. The document itself was marked as confidential.

**Result:**
A confidential document was accessible through the publicly exposed directory without appropriate access restrictions.

**Security Impact:**
Public exposure of confidential documents can disclose sensitive business information to unauthorized users.

**Recommendation:**
Do not expose sensitive files through publicly accessible directories. Apply appropriate access controls, remove unnecessary files from web-accessible locations, and configure the server to prevent directory listing where it is not required.

**Evidence:**
Screenshot: 04-sensitive-data-exposure.png
