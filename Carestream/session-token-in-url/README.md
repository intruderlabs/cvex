# Session Token In URL

### Product Description:
The Clinical Collaboration Platform is designed for the healthcare sector. It provides advanced tools to consolidate, manage, and share medical images and reports seamlessly across healthcare organizations of any size.
	
### Vulnerability Description:
The web application uses the HTTP GET method to process a request and includes sensitive information in the query string of that request.

### Vulnerability Type:
CWE-598: Use of GET Request Method With Sensitive Query Strings

### Example vulnerable URL 
    https://example[.]com/default.aspx?usertoken=SESSION_TOKEN_HERE
	
### Vendor:
Carestream Health, Inc.
	
### Affected Product:
Clinical Collaboration Platform V12.2.1.5
Probably previous are also affected
	
### Affected Component:
Session Token

### Attack Vector:
Remote
	
### Code Execution:
No
	
### Attack Vector:
An attacker can exploit this vulnerability by intercepting requests or accessing browsing history to obtain confidential data, compromising the application's privacy and security.
	
### Reference:
- https://cwe.mitre.org/data/definitions/598.html
- https://portswigger.net/kb/issues/00500700_session-token-in-url
	
### Discoverer:
Kauan Akyra (Ak7r4) | kakyra@intruderlabs.com.br
