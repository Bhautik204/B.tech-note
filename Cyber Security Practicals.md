# SQL Injection
## Platforms for practising SQL Injection:
1. **Damn Vulnerable Web Application(DVWA):**
	- PHP/MySQL website intentionally designed to vulnerable
	- [Visit here](https://buydomainnames.co.uk/domain/dvwa.co.uk?offer=parked)
2. **bWAPP**:
    - A buggy web application for testing web security knowledge.
    - [Visit here](http://www.itsecgames.com/)
3.  **OWASP Juice Shop**:
    - A modern application with intentionally included vulnerabilities, including SQL injection.
    - [Visit here](https://owasp.org/www-project-juice-shop/)
4. **Hack The Box**:
    - Offers realistic penetration testing challenges in a controlled environment.
    - [Visit here](https://www.hackthebox.com/)
5. **TryHackMe**:
    - A learning platform with hands-on labs focused on cyber security topics, including SQL injection.
    - [Visit here](https://tryhackme.com/)
6. **WebGoat**:
    - An educational tool from OWASP, teaching about web application security vulnerabilities.
    - Visit here
7. **SQL Injection Playground by PentesterLab**:
    - Dedicated labs for SQL injection practice.
    - [Visit here](https://pentesterlab.com/)

1.  [Test PHP Vulnerable Web](http://testphp.vulnweb.com/)**

- A live, intentionally vulnerable website provided by Acunetix.
- Designed for practicing web application security testing.
- URL: [http://testphp.vulnweb.com/](http://testphp.vulnweb.com/)

---

2. [Peruggia](http://www.webscantest.com/)**

- A deliberately insecure web application built for security testing.
- URL: [http://www.webscantest.com/](http://www.webscantest.com/)

---
3. [SQL Injection Practice Sites by PortSwigger Labs](https://portswigger.net/web-security/sql-injection)**

- Provides multiple intentionally vulnerable challenges.
- You need to register for free access.
- URL: [https://portswigger.net/web-security/sql-injection](https://portswigger.net/web-security/sql-injection)

- altoroMutual 
- testphp.vulnweb.com

## sqlmap
#### features
- their is 6 SQL injection technique.
- when we find vulnerable database,time of password extraction it will be also find which type hashed is used in encryption. 
- we can dump all table of database
#### overview
- technique
	- B: Boolean-based blind
	- E: Error-based
	- U: Union query-based
	- S: stacked queries
	- T: Time-based blind
	- Q: Inline queries
	ex: --technique-"B" 
- crawl
	- it a parameter, which is scan whole website and then it tell which parameter is vulnerable
	- their is depth in crawl , which is tell how many directory explore. 
- enumeration
- batch
- risk
- level
- thread
- verbosity
- proxy
- SQL injection via burp-suite
- -u
	- use to provide URL of website
-  --forms
-  --data
- --header
- --user-agent
- --cookie
- --flush-session
- --output-dir
- --temper

## Step & explanation of sqlmap cmd
1. 