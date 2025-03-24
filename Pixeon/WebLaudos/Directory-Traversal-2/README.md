# Directory Traversal
### Product Description:
The WebLaudos software developed by Pixeon is a system that manage, and share medical images that can be accessed by doctors or patients.

### Vulnerability Description:
A path traversal attack (also known as directory traversal) was discovered in the WebLaudos software. This vulnerability allows an attacker to access files and directories stored outside the web root folder. By manipulating the id parameter in the URL using “dot-dot-slash (../)” sequences and their variations or by using absolute file paths, an attacker may be able to access arbitrary files and directories on the file system, including system files.

### Vulnerability Type:
CWE-35: Path Traversal

### Example vulnerable URL
The first directories are customizable, so here are three examples of vulnerable URLs: <br>
https://example.com/laudo/select-gen/get_async_info.asp <br>

https://example.com/web_laudos/select-gen/get_async_info.asp <br>

https://example.com/select-gen/get_async_info.asp <br>


### Vendor:
Pixeon

### Affected Product:
WebLaudos — 24.2 (04)

### Affected Component: <br>
Endpoint: select-gen/get_async_info.asp <br>
Parameter (POST): file <br>
Example payload: file=%2e%2e%5c%5c%2e%2e%5c%5cWindows%5csystem32%5cdrivers%5cetc%5chosts <br>

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
Alan Lacerda | alacerda@intruderlabs.com.br
