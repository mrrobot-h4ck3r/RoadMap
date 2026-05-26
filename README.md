# 🛣️ Roadmap to Bug Bounty Hunting

## From Absolute Beginner to Bug Bounty Ready

**Created by:** mrrobot_h4ck3r  
**Format:** GitHub Markdown Ready

---

## 📑 Table of Contents

- [Phase 0: Prerequisites & Mindset](#phase-0-prerequisites--mindset)
- [Phase 1: Linux Fundamentals](#phase-1-linux-fundamentals)
- [Phase 2: Networking Basics](#phase-2-networking-basics)
- [Phase 3: Web Technologies](#phase-3-web-technologies)
- [Phase 4: Tools of the Trade](#phase-4-tools-of-the-trade)
- [Phase 5: Vulnerability Labs (Core 5)](#phase-5-vulnerability-labs-core-5)
- [Phase 6: Recon & OSINT](#phase-6-recon--osint)
- [Phase 7: Advanced Vulnerabilities](#phase-7-advanced-vulnerabilities)
- [Phase 8: Practice Platforms](#phase-8-practice-platforms)
- [Phase 9: Go Live - Bug Bounties](#phase-9-go-live---bug-bounties)
- [Appendix: Quick Commands Cheat Sheet](#appendix-quick-commands-cheat-sheet)
- [Weekly Study Plan](#weekly-study-plan)

---

## Phase 0: Prerequisites & Mindset

> **Golden Rule:** Never test on websites you don't own or don't have written permission for.

### Requirements

| Requirement | Time |
|-------------|------|
| Basic computer literacy | 1 day |
| Willingness to read docs | Ongoing |
| Firefox browser (for Burp integration) | 10 min |

---

## Phase 1: Linux Fundamentals

**Why:** 90% of bug hunting tools run on Linux. You need the terminal.

### What to Learn

| Command Category | Commands |
|------------------|----------|
| Navigation | `ls`, `cd`, `pwd`, `tree` |
| File operations | `cp`, `mv`, `rm`, `touch`, `cat`, `nano`, `vim` |
| Permissions | `chmod`, `chown`, `sudo` |
| Processes | `ps`, `top`, `kill`, `htop` |
| Networking | `curl`, `wget`, `netstat`, `ss` |
| Piping/Redirection | `\|`, `>`, `>>`, `grep`, `awk`, `sed` |

### 🧪 Free Labs

| Platform | Link | Coverage |
|----------|------|----------|
| TryHackMe - Linux Fundamentals | [https://tryhackme.com/module/linux-fundamentals](https://tryhackme.com/module/linux-fundamentals) | Complete beginner |
| OverTheWire - Bandit | [https://overthewire.org/wargames/bandit/](https://overthewire.org/wargames/bandit/) | 34 CLI levels |
| Linux Journey | [https://linuxjourney.com/](https://linuxjourney.com/) | Theory + interactive |
| TryHackMe - Linux PrivEsc | [https://tryhackme.com/room/linuxprivesc](https://tryhackme.com/room/linuxprivesc) | Advanced |

### ✅ Completion Checklist

- [ ] Navigate, create/delete files, edit text in terminal
- [ ] Understand `chmod 755 filename`
- [ ] Complete Bandit levels 0–10

---

## Phase 2: Networking Basics

**Why:** Web security requires understanding how data travels.

### What to Learn

- OSI Model (Layers 4 & 7)
- TCP vs UDP
- HTTP/HTTPS (methods, status codes, headers, cookies)
- DNS (domain → IP, record types)
- Proxies (Burp Suite as MITM)

### Important HTTP Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK - Success |
| 301/302 | Redirect |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 405 | Method Not Allowed |
| 429 | Too Many Requests (test this!) |
| 500 | Internal Server Error |

### 🧪 Free Labs

| Platform | Link | Topic |
|----------|------|-------|
| TryHackMe - Intro to Networking | [https://tryhackme.com/room/introtonetworking](https://tryhackme.com/room/introtonetworking) | Beginner networking |
| TryHackMe - HTTP in Detail | [https://tryhackme.com/room/httpindetail](https://tryhackme.com/room/httpindetail) | HTTP methods/headers |
| TryHackMe - DNS in Detail | [https://tryhackme.com/room/dnsindetail](https://tryhackme.com/room/dnsindetail) | DNS deep dive |
| PortSwigger - HTTP Protocol | [https://portswigger.net/web-security/http](https://portswigger.net/web-security/http) | HTTP deep dive |
| TryHackMe - Wireshark | [https://tryhackme.com/room/wireshark](https://tryhackme.com/room/wireshark) | Packet analysis |

### ✅ Completion Checklist

- [ ] Explain what happens when you type `google.com` in a browser
- [ ] Identify HTTP methods and status codes in Burp
- [ ] Understand cookies and session headers

---

## Phase 3: Web Technologies

**Why:** You cannot break what you do not understand.

### Priority Learning

| Priority | Technology | What to Know |
|----------|------------|--------------|
| High | HTML | Forms, attributes, DOM structure |
| High | JavaScript | Syntax, DOM manipulation, fetch API |
| High | JSON | Structure, parsing, API usage |
| Medium | Python | Requests library, automation scripts |
| Medium | PHP | Super globals (`$_GET`, `$_POST`) |
| Low | CSS | Basic UI understanding |

### 🧪 Free Labs

| Platform | Link | Topic |
|----------|------|-------|
| W3Schools - HTML | [https://www.w3schools.com/html/](https://www.w3schools.com/html/) | HTML basics |
| W3Schools - JavaScript | [https://www.w3schools.com/js/](https://www.w3schools.com/js/) | JS fundamentals |
| TryHackMe - JavaScript Basics | [https://tryhackme.com/room/javascriptbasics](https://tryhackme.com/room/javascriptbasics) | Interactive JS |
| TryHackMe - Python for Pentesters | [https://tryhackme.com/room/pythonforpentesters](https://tryhackme.com/room/pythonforpentesters) | Python for hacking |
| TryHackMe - PHP for Hackers | [https://tryhackme.com/room/php](https://tryhackme.com/room/php) | PHP security |

### ✅ Completion Checklist

- [ ] Read HTML and spot input forms
- [ ] Understand what `<script>alert(1)</script>` does
- [ ] Write a simple Python script using `requests.get()`

---

## Phase 4: Tools of the Trade

### Essential Tools

| Tool | Purpose | Learning Link |
|------|---------|---------------|
| Burp Suite Community | Intercept/modify HTTP traffic | [PortSwigger Academy](https://portswigger.net/web-security) |
| Nmap | Network scanning | [TryHackMe Nmap](https://tryhackme.com/room/furthernmap) |
| Gobuster/Dirb | Directory brute-forcing | [TryHackMe Gobuster](https://tryhackme.com/room/gobuster) |
| curl | HTTP from terminal | Built into Linux |
| jq | Parse JSON in terminal | `sudo apt install jq` |

### 🧪 Free Tool Labs

| Platform | Link | Tool |
|----------|------|------|
| TryHackMe - Burp Suite Basics | [https://tryhackme.com/room/burpsuitebasics](https://tryhackme.com/room/burpsuitebasics) | Burp Suite |
| PortSwigger - Burp Tutorial | [https://portswigger.net/burp/documentation/desktop/getting-started](https://portswigger.net/burp/documentation/desktop/getting-started) | Burp Suite |
| TryHackMe - Nmap | [https://tryhackme.com/room/nmap01](https://tryhackme.com/room/nmap01) | Nmap |
| TryHackMe - Advanced Nmap | [https://tryhackme.com/room/nmap02](https://tryhackme.com/room/nmap02) | Advanced Nmap |

### Burp Suite Workflow

1. **Proxy** → Intercept on
2. **Repeater** → Modify and resend requests
3. **Intruder** → Brute-force parameters
4. **Comparer** → Compare two responses

---

## Phase 5: Vulnerability Labs (Core 5)

> ⚠️ **Do not move to advanced until comfortable with all 5.**

---

### 1. IDOR (Insecure Direct Object Reference)

| Type | Link |
|------|------|
| Theory | [PortSwigger IDOR](https://portswigger.net/web-security/access-control/idor) |
| Lab (Easy) | [PortSwigger IDOR Lab 1](https://portswigger.net/web-security/access-control/lab-idor) |
| Lab (Medium) | [PortSwigger IDOR Lab 2](https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter) |
| Practice | [TryHackMe IDOR](https://tryhackme.com/room/idor) |

---

### 2. SQL Injection (SQLi)

| Type | Link |
|------|------|
| Theory | [PortSwigger SQLi](https://portswigger.net/web-security/sql-injection) |
| Lab (Error-based) | [PortSwigger SQLi Lab 1](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data) |
| Lab (Union-based) | [PortSwigger SQLi Union](https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-columns) |
| Lab (Blind SQLi) | [PortSwigger Blind SQLi](https://portswigger.net/web-security/sql-injection/blind/lab-conditional-responses) |
| Practice | [TryHackMe SQLi](https://tryhackme.com/room/sqlinjection) |

---

### 3. Cross-Site Scripting (XSS)

| Type | Link |
|------|------|
| Theory | [PortSwigger XSS](https://portswigger.net/web-security/cross-site-scripting) |
| Lab (Reflected) | [PortSwigger Reflected XSS](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded) |
| Lab (Stored) | [PortSwigger Stored XSS](https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded) |
| Lab (DOM-based) | [PortSwigger DOM XSS](https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-document-write-sink) |
| Practice | [TryHackMe XSS](https://tryhackme.com/room/xss) |

---

### 4. CSRF (Cross-Site Request Forgery)

| Type | Link |
|------|------|
| Theory | [PortSwigger CSRF](https://portswigger.net/web-security/csrf) |
| Lab (Basic) | [PortSwigger CSRF Lab 1](https://portswigger.net/web-security/csrf/lab-no-defenses) |
| Lab (Token Bypass) | [PortSwigger CSRF Token Bypass](https://portswigger.net/web-security/csrf/lab-token-validation-depends-on-request-method) |
| Practice | [TryHackMe CSRF](https://tryhackme.com/room/csrf) |

---

### 5. Broken Authentication

| Type | Link |
|------|------|
| Theory | [PortSwigger Auth](https://portswigger.net/web-security/authentication) |
| Lab (Password reset) | [PortSwigger Password Reset](https://portswigger.net/web-security/authentication/other-mechanisms/lab-password-reset-poisoning-via-middleware) |
| Lab (Brute-force) | [PortSwigger Brute-force](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses) |
| Practice | [TryHackMe Auth Bypass](https://tryhackme.com/room/authenticationbypass) |

---

## Phase 6: Recon & OSINT

> You cannot find bugs you do not see.

### Recon Tools

| Tool | Purpose | Link |
|------|---------|------|
| Subfinder | Subdomain enumeration | [GitHub](https://github.com/projectdiscovery/subfinder) |
| Assetfinder | Subdomain tool | [GitHub](https://github.com/tomnomnom/assetfinder) |
| Gau | URLs from Wayback Machine | [GitHub](https://github.com/lc/gau) |
| Katana | Crawl JS files | [GitHub](https://github.com/projectdiscovery/katana) |
| Hakrawler | Discover endpoints | [GitHub](https://github.com/hakluke/hakrawler) |
| LinkFinder | Find JS endpoints | [GitHub](https://github.com/GerbenJavado/LinkFinder) |
| FFUF | Directory fuzzing | [GitHub](https://github.com/ffuf/ffuf) |

### Sample Recon Workflow

```bash
# 1. Subdomains
subfinder -d target.com -o subs.txt
assetfinder target.com >> subs.txt

# 2. Alive check
cat subs.txt | httpx -o alive.txt

# 3. Get URLs
cat alive.txt | gau | grep -E "\.js|\.php|\.asp|\.json" > urls.txt

# 4. Fuzz directories
ffuf -u https://target.com/FUZZ -w /usr/share/wordlists/dirb/common.txt

```
## Phase 7: Advanced Vulnerabilities

> After mastering Phases 5 & 6.

| Vulnerability | Best Free Lab |
|---------------|---------------|
| SSRF | [PortSwigger SSRF Labs](https://portswigger.net/web-security/ssrf) |
| XXE | [PortSwigger XXE Labs](https://portswigger.net/web-security/xxe) |
| Subdomain Takeover | [TryHackMe Subdomain Takeover](https://tryhackme.com/room/subdomaintakeover) |
| API Security | [TryHackMe API Hacking](https://tryhackme.com/room/apihacking) |
| JWT Attacks | [PortSwigger JWT Labs](https://portswigger.net/web-security/jwt) |
| NoSQL Injection | [PortSwigger NoSQL Labs](https://portswigger.net/web-security/nosql-injection) |

---

## Phase 8: Practice Platforms

| Platform | Link | Best For |
|----------|------|----------|
| TryHackMe | [https://tryhackme.com](https://tryhackme.com) | Absolute beginners |
| PortSwigger Academy | [https://portswigger.net/web-security](https://portswigger.net/web-security) | Deep vulnerability understanding |
| HackTheBox Academy | [https://academy.hackthebox.com](https://academy.hackthebox.com) | Advanced learners |
| OWASP Juice Shop | [https://owasp.org/www-project-juice-shop/](https://owasp.org/www-project-juice-shop/) | Self-hosted practice |
| PentesterLab | [https://pentesterlab.com](https://pentesterlab.com) | Hands-on exercises |
| Root-Me | [https://www.root-me.org](https://www.root-me.org) | Challenges by category |

---

## Phase 9: Go Live - Bug Bounties

> ⚠️ **Only after completing Phases 1–8.**

### Beginner-friendly Bounty Platforms

| Platform | Link | Notes |
|----------|------|-------|
| HackerOne | [https://hackerone.com](https://hackerone.com) | Large, structured |
| Bugcrowd | [https://bugcrowd.com](https://bugcrowd.com) | Beginner programs exist |
| Intigriti | [https://intigriti.com](https://intigriti.com) | EU focus |

### Beginner-friendly Programs

| Program | Platform | Type | Why |
|---------|----------|------|-----|
| Yahoo | HackerOne | VDP | Safe practice, no bounty |
| GitLab | HackerOne | Bug Bounty | Good scope docs |
| Shopify | HackerOne | Bug Bounty | Well-documented |
| WordPress | Bugcrowd | Bug Bounty | High traffic, many bugs |

> **Important:** Start with **VDPs (Vulnerability Disclosure Programs)**. No money, but legal and excellent practice.

---

## Appendix: Quick Commands Cheat Sheet

### Linux Commands

```bash
# Find files with sensitive info
grep -r "api_key" /var/www/
find . -name "*.env"

# Check open ports
netstat -tulpn
ss -tulpn

# Download a file
curl -O https://example.com/file
wget https://example.com/file
```


# Recon Commands
# Subdomains
subfinder -d target.com | tee subs.txt
assetfinder target.com >> subs.txt

# Alive check
cat subs.txt | httpx -status-code -follow-redirects

# Grab URLs with parameters
gau target.com | grep "=" | tee params.txt

# Directory fuzzing
ffuf -u https://target.com/FUZZ -w /usr/share/wordlists/seclists/Discovery/Web-Content/common.txt


## Weekly Study Plan
Week	Focus	Daily Time
1	Linux + TryHackMe Pre-Security	1-2 hours
2	Networking + HTTP Deep Dive	1-2 hours
3	Web Technologies (HTML, JS, Python)	1-2 hours
4	Burp Suite + Tools	2 hours
5	IDOR + SQL Injection (Labs)	2 hours
6	XSS + CSRF + Broken Authentication	2 hours
7	Recon (Subdomains, JS Analysis)	2-3 hours
8	Advanced + Live VDP Practice	2-3 hours
