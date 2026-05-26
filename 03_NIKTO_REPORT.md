NIKTO Web Server Scan Report

Target Information
- Target URL: http://localhost:3000
- Scan Tool: Nikto
- Scan Date: [Add Date]
- Tester: [Your Name]



Scan Summary

Nikto was used to scan the local web server running on port 3000 to identify common web server vulnerabilities, insecure configurations, and information disclosure issues.



Findings

1. Missing Security Headers

The following important HTTP security headers were missing:

- X-Frame-Options
- X-Content-Type-Options
- Content-Security-Policy
- Strict-Transport-Security

Risk
Missing security headers can expose the application to:
- Clickjacking attacks
- MIME sniffing attacks
- Cross-site scripting (XSS)
- SSL stripping attacks

Recommendation
Configure the web server or application to include proper security headers.


2. Server Information Disclosure

Nikto detected that the server discloses information through HTTP headers.


- Server: Express
- X-Powered-By: Express

Attackers can identify the server technology and version to target known vulnerabilities.

Disable or hide unnecessary server banners and headers.


3. Dangerous or Sensitive Files

Nikto identified potentially sensitive files or directories accessible on the server.

Example
- /robots.txt
- /admin
- Backup or configuration files

Risk
Sensitive files may expose internal information or administrative functionality.

Recommendation
Restrict access to sensitive files and remove unnecessary resources.

---

Weak Server Configuration

The scan identified weak or insecure configurations.

Examples
- Directory indexing enabled
- Default pages present
- Insecure HTTP methods allowed

Risk
Weak configurations increase the attack surface of the application.

Recommendation
Disable unnecessary HTTP methods and harden server configuration.


Conclusion

The Nikto scan identified several security weaknesses in the local web server, including missing security headers, information disclosure, dangerous files, and weak configurations. Proper hardening and secure configuration practices are recommended to reduce security risks.

 