# Session Token In URL

### Product Description:
The Clinical Collaboration Platform is designed for the healthcare sector. It provides advanced tools to consolidate, manage, and share medical images and reports seamlessly across healthcare organizations of any size.
	
### Vulnerability Description:
3 vulnerabilities were found:
- Session token being sent using the GET method
- Session hijacking; if an attacker gains access to the URL containing the session token, they will be able to impersonate the user's account, as there are no protections against session hijacking.
- Weak logout system; even after logging out, the session token remains valid

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
