# Directory Traversal

### Product Description:
The WebLaudos software developed by Pixeon is a system that manage, and share medical images that can be accessed by doctors or patients.
	
### Vulnerability Description:
A path traversal attack (also known as directory traversal) was discovered in the WebLaudos software. This vulnerability allows an attacker to access files and directories stored outside the web root folder. By manipulating the id parameter in the URL using “dot-dot-slash (../)” sequences and their variations or by using absolute file paths, an attacker may be able to access arbitrary files and directories on the file system, including system files.

### Vulnerability Type:
CWE-35: Path Traversal: '.../...//'

### Example vulnerable URL 
The first directories are customizable, so here are three examples of vulnerable URLs:
https://example.com/laudo/multimagem/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts
https://example.com/web_laudos/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts
https://example.com/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts
	
### Vendor:
Pixeon
	
### Affected Product:
WebLaudos — 24.2 (04)
	
### Affected Component:
Endpoint: https://example.com/laudo/multimagem/img/img-cache.asp
Parameter: id

### Attack Vector:
Remote
	
### Code Execution:
No
	
### Attack Vector:
Attackers can escape outside of the restricted location to access files or directories that are elsewhere on the system.
	
### Reference:
https://cwe.mitre.org/data/definitions/35.html
https://cwe.mitre.org/data/definitions/22.html
https://owasp.org/www-community/attacks/Path_Traversal
	
### Discoverer:
Kauan Akyra (Ak7r4) | kakyra@intruderlabs.com.br
