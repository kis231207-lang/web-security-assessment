Finding 01 – Product Tampering

Application:
OWASP Juice Shop

Target:
Local OWASP Juice Shop (localhost:3000)

Product:
OWASP SSL Advanced Forensic Tool (O-Saft)

Product ID:
9

Tool Used:
Postman

Vulnerability Category:
API Security / Improper Authorization

Description:
During testing, the product API was found to accept a PUT request
that modified the description of product ID 9.

Testing:
A PUT request was sent to the local Juice Shop API endpoint:

/api/Products/9

The product description was changed to contain a different link.

Result:
The server returned a successful response and the modified
product information was returned.

Security Impact:
If an application allows unauthorized users to modify product
information, an attacker could alter application data.

Recommendation:
Implement proper authentication and authorization checks on
product update API endpoints. Only users with the required
permissions should be allowed to modify product information.

Evidence:
Screenshot: 01-product-tampering.png