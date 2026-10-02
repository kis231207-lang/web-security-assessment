# Finding 02 – SQL Injection

**Application:**
OWASP Juice Shop

**Target:**
Local OWASP Juice Shop (localhost:3000)

**Tool Used:**
Web Browser

**Vulnerability Category:**
SQL Injection

**Description:**
During testing, the login form was found to be vulnerable to SQL Injection. A specially crafted input in the email field caused the application to accept the login request without a valid user password.

**Testing:**
The login form was tested using SQL injection input in the email field while using a test password.

**Result:**
The application successfully logged in, demonstrating that the login input was not properly protected against SQL injection.

**Security Impact:**
An SQL Injection vulnerability in an authentication function could allow an attacker to bypass normal authentication controls and potentially access protected application functionality.

**Recommendation:**
Use parameterized queries or prepared statements for database operations. Validate and sanitize user input and implement secure authentication controls.

**Evidence:**
Screenshot: 02-sql-injection.png
