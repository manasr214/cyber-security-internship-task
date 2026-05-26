# Directory Enumeration Report

## Target Information

| Item | Details |
|---|---|
| Target URL | http://localhost:3000 |
| Tool Used | Gobuster |
| Enumeration Type | Directory Enumeration |

---

# Command Used

gobuster dir -u http://localhost:3000 -w /usr/share/wordlists/dirb/common.txt

---

# Discovered Directories and Endpoints

| Directory / Endpoint | Observation |
|---|---|
| /assets | Static application assets directory discovered |
| /rest | REST API endpoint identified |
| /api | API route detected |
| /ftp | Public FTP directory identified |
| /robots.txt | Robots file exposed |

---

# Security Observations

- Multiple accessible endpoints were identified.
- REST API routes were publicly accessible.
- Static asset directories were visible.
- Potentially sensitive endpoints were exposed during enumeration.

---

# Findings

| Finding | Description |
|---|---|
| Public API Exposure | REST endpoints accessible without authentication |
| Visible Static Directories | Application asset directories exposed |
| Information Disclosure | robots.txt file publicly accessible |
| Directory Enumeration Successful | Multiple hidden paths identified |

---

# Conclusion

Gobuster successfully identified multiple directories, API endpoints, and publicly accessible resources within the OWASP Juice Shop application running on localhost.