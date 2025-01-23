# SQL Injection
## Platforms for practising SQL Injection:
1. **Damn Vulnerable Web Application(DVWA):**
	- PHP/MySQL website intentionally designed to vulnerable
	- [Visit here](https://buydomainnames.co.uk/domain/dvwa.co.uk?offer=parked)
2. **bWAPP**:
    - A buggy web application for testing web security knowledge.
    - [Visit here](http://www.itsecgames.com/)
3.  **O+WASP Juice Shop**:
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
	- if we find vulnerable url then how we exploit website and find useful data.
	- when we give vulnerability report, we have to show which type of data we have, so that give high impact to report.
- risk
	- when we not find vulnerability, we have to try different payloads
	- 1(by default) : payload we use doesn't harm server
	- 2 : it also use Time-based SQL injection
	- 3 : it try OR-based SQL injection, as a parameter also use update command and put as payload in database. it's so harmful that if it hit database it will update database,table and data.
- level
	- when we testing a website, sometimes we not find vulnerability.
	- if we level up to 2 it goes into cookie and test it and is their any vulnerability?
	- if we use level 3 it goes into user-agent and test it.
	- higher the level , vulnerability impact and test range goes high.
	- 1 is default and 5 is max 
- thread 
	- when website is larger, you can tell how many connection should use. by default: 1 and max: 10
- verbosity
	- it give option that if SQL injection is perform on any website , we can fetch the details.
	- 0 : show only Python tracebacks, error and critical messages.
	- 1 : show information and warning messages.
	- 2 : show debug messages.
	- 3 : show payload injected.
	- 4 : show HTTP requests.
	- 5 : show HTTP responses headers.
	- 6 : show HTTP responses page content.
- batch
- proxy
- SQL injection via burp-suite
- -u (use to provide URL of website)
- --current-user (give current user name)
- --current-db (to see current database)
- --hostname (to identify hostname/system name )
- 
- --batch (to select by default option of questions)
- --dbs (give details of all available database)
- -D (to select specific database from list)
- --table (give details of all table in selected database)
- -T (to select specific table from tables)
- --dump (to see all data of table)
- --columns (to see datatypes of columns in table)
-  --forms
-  --data
- --header
- --user-agent
- --cookie
- --flush-session
- --output-dir
- --temper

## reference
https://youtu.be/QsMkQMKsIII?si=S6O61COEgzBIuZtn

