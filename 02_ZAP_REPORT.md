# ZAP REPORT

## TARGET INFO

| Item | Details |
|---|---|
| Target URL | http://localhost:3000 |
| Tool Used | OWASP ZAP |
| Scan Type | Automated Scan |

---

# Vulnerabilities Identified

| Vulnerability | Severity | Description | Recommendation |
|---|---|---|---|
| CSP: Failure to Define Directive with No Fallback | Medium | The Content Security Policy failed to define certain directives, allowing unrestricted content loading. | Configure proper Content Security Policy directives with secure fallback rules. |
| Cross-Domain Misconfiguration | Medium | Cross-Origin Resource Sharing (CORS) was configured with wildcard access permissions. | Restrict Access-Control-Allow-Origin to trusted domains only. |
| Timestamp Disclosure - Unix | Low | Unix timestamp information was disclosed by the server/application. | Limit unnecessary information disclosure from server responses. |

---

# Detailed Findings

## 1. CSP: Failure to Define Directive with No Fallback

- Risk Level: Medium  
- URL: http://localhost:3000/assets  
- Alert Reference: 10055-1  

### Description

The Content Security Policy failed to define one or more directives that do not have fallback protections. This may allow unrestricted content execution or loading.

### Recommendation

- Define all required CSP directives properly.
- Implement secure fallback policies.
- Restrict external resource loading.

---

## 2. Cross-Domain Misconfiguration

- Risk Level: Medium  

### Evidence

```txt
Access-Control-Allow-Origin: *