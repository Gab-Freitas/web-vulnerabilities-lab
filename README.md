# 🛡️ Vulnerable PyFlaSQL - Security Lab
This project is an intentionally vulnerable web application built with Python and Flask. It was developed as part of a hands-on security lab to demonstrate and explore three common web vulnerabilities from the [OWASP Top 10](https://owasp.org/www-project-top-ten):

- SQL Injection (A03:2021)
- Broken Authentication (A01:2021)
- Cross-Site Scripting (XSS) (A07:2021)

- ## 🔍 Purpose

The goal of this project is to:

- Understand how web vulnerabilities emerge during development
- Practice exploiting them using tools like Burp Suite and browser dev tools
- Learn how to properly secure web applications by applying appropriate mitigations


## 🧪 Vulnerabilities Implemented

### 1. SQL Injection

**Vulnerable Endpoint**: `/login`  
**Exploit**: Bypass authentication with payloads like `' OR '1'='1`  
**Fix**: Use parameterized queries instead of string concatenation

### 2. Broken Authentication

**Vulnerable Feature**: No session management or role verification  
**Exploit**: Direct access to protected routes or tampered cookies  
**Fix**: Implement secure session handling and role-based access control

### 3. Cross-Site Scripting (XSS)

**Vulnerable Page**: `/comments`  
**Exploit**: Inject JavaScript like `<script>alert("XSS")</script>`  
**Fix**: Properly escape user input and use security headers (e.g., CSP)

## 🛠 Tools Used

- Python 3.x
- Flask
- SQLite
- Burp Suite
- Web browser (Dev Tools)
