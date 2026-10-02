# Web Application Security Assessment

## Overview

This project presents a controlled security assessment of the intentionally vulnerable OWASP Juice Shop training application.

The assessment identified four security findings across authorization, authentication, client-side scripting, and information disclosure.

> **Scope:** This assessment was performed only against a locally hosted OWASP Juice Shop instance running on `localhost:3000`. The findings and evidence must not be interpreted as an assessment of any production or third-party system.

## Objectives

- Understand common web application security weaknesses
- Perform controlled security testing
- Capture evidence of observed behavior
- Assess potential security impact
- Document practical remediation recommendations

## Methodology

The assessment followed a controlled workflow:

1. Identify application functionality
2. Test the functionality locally
3. Observe application responses
4. Classify the security weakness
5. Assess the potential impact
6. Document remediation recommendations

## Findings

| ID | Finding | Category | Observation |
|---|---|---|---|
| 01 | Product Tampering | API Authorization | A product update request modified product information and returned successfully. |
| 02 | SQL Injection | Authentication | Crafted SQL input in the login field was accepted without a valid password. |
| 03 | Cross-Site Scripting (XSS) | Client-Side Injection | A harmless test payload in the search function triggered JavaScript execution. |
| 04 | Sensitive Data Exposure | Information Disclosure | A publicly accessible `/ftp` directory exposed a confidential document. |

## Tools Used

- Web Browser
- Browser Developer Tools
- Postman
- OWASP Juice Shop
- Docker

## Remediation Summary

### 1. Authentication
Use parameterized queries or prepared statements, validate inputs, and ensure authentication controls cannot be bypassed.

### 2. Authorization
Apply authentication and permission checks to sensitive API endpoints and restrict modifications to appropriately authorized users.

### 3. Client-Side Execution
Use context-appropriate output encoding and safe input handling. A strong Content Security Policy should also be considered where appropriate.

### 4. Information Exposure
Remove sensitive files from publicly accessible directories, apply appropriate access controls, and disable unnecessary directory listing.

## Evidence

The repository contains:

- Security finding documentation
- Screenshots from the local assessment
- Final assessment report

See `REPORT.pdf` for the complete assessment report.

## Conclusion

The assessment provided practical experience in identifying, testing, documenting, and recommending remediation for common web application security weaknesses.

All testing was conducted against the intentionally vulnerable OWASP Juice Shop training environment and was strictly bounded to `localhost:3000`.
