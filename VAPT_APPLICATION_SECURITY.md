# Specialization Guide: Vulnerability Assessment & Penetration Testing (VAPT) / AppSec

[![Track](https://img.shields.io/badge/Track-Offensive%20Security%20%7C%20VAPT%20%7C%20AppSec-red.svg)](#)
[![Hands--On](https://img.shields.io/badge/Skills-Hands--On%20Web%20%26%20Network%20Exploitation-orange.svg)](#)
[![Cost](https://img.shields.io/badge/Lab%20Cost-%E2%82%B90%20(Free--First)-purple.svg)](#)

A comprehensive, operational deep dive into **Vulnerability Assessment and Penetration Testing (VAPT), Web Application Security (AppSec), and Ethical Hacking**. This guide explains how offensive security teams discover and exploit software vulnerabilities, provides a full hands-on lab on Windows 11 (zero router access needed), details the seniority progression from Junior VAPT Analyst to Head of Offensive Security, and maps out general and specialized certifications.

---

## Table of Contents
1. [How VAPT & Application Security Actually Work](#1-how-vapt--application-security-actually-work)
2. [Daily Operational Workflows (Scoping, Testing, PoC, Remediation)](#2-daily-operational-workflows-scoping-testing-poc-remediation)
3. [Dedicated Hands-On Lab Blueprint (Windows 11 | Local Vulnerable App)](#3-dedicated-hands-on-lab-blueprint-windows-11--local-vulnerable-app)
4. [Seniority Level Progression & Career Ladder](#4-seniority-level-progression--career-ladder)
5. [Certification Roadmap (General & Specialization-Specific)](#5-certification-roadmap-general--specialization-specific)

---

## 1. How VAPT & Application Security Actually Work

VAPT is the discipline of **authorized, simulated cyberattacks** designed to find and fix security weaknesses before real adversaries exploit them.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        PHASE 1: SCOPING & RECONNAISSANCE               │
│               (Target URLs, IP Ranges, Rules of Engagement)            │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Passive/Active Enumeration
┌───────────────────────────────────▼────────────────────────────────────┐
│                    PHASE 2: VULNERABILITY ASSESSMENT (VA)              │
│       (Automated Scanners: Nessus / Nikto / Burp Active Scanner)       │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Candidate Vulnerabilities
┌───────────────────────────────────▼────────────────────────────────────┐
│                    PHASE 3: PENETRATION TESTING (PT)                   │
│   (Manual Exploit Verification: Parameter Tampering / SQLi / IDOR)     │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Confirmed Proof-of-Concept (PoC)
┌───────────────────────────────────▼────────────────────────────────────┐
│                    PHASE 4: REPORTING & REMEDIATION                    │
│      (CVSS v3.1 Scoring, Developer Code Fixes, Re-Testing Verification)│
└────────────────────────────────────────────────────────────────────────┘
```

### The Difference Between VA and PT
* **Vulnerability Assessment (VA):** Broad and automated. Scanners sweep IP ranges and web endpoints, matching software versions and banner strings against known CVE databases. It identifies *potential* weaknesses but produces false positives.
* **Penetration Testing (PT):** Deep and manual. A human security tester attempts to actively exploit those weaknesses, chain multiple minor bugs together (e.g. CSRF ➔ Account Takeover), and prove real business impact (stealing customer data or gaining administrative access).

### The OWASP Top 10 Vulnerabilities
The Open Web Application Security Project (OWASP) defines the critical security risks in modern web applications:
1. **Broken Access Control (IDOR / BOLA):** Users can access records belonging to other users simply by tampering with an ID parameter in the URL or API request (e.g., changing `/api/user/101/profile` to `/api/user/102/profile`).
2. **Cryptographic Failures:** Transmitting sensitive data over unencrypted HTTP, or storing passwords using weak algorithms (MD5, SHA-1) instead of salted bcrypt/argon2.
3. **Injection (SQLi, Command Injection):** Untrusted user input is directly concatenated into a database query or system command without parameterization.
4. **Insecure Design:** Fundamental architectural flaws that no amount of code patching can fix (e.g., lacking rate-limiting on password reset endpoints).
5. **Security Misconfiguration:** Default passwords enabled, debug error messages exposing stack traces, open directory listings.
6. **Vulnerable and Outdated Components:** Using old open-source libraries or npm/pip packages with known exploits.
7. **Identification and Authentication Failures:** Allowing brute-force attacks, weak password policies, or session fixation.
8. **Software and Data Integrity Failures:** Auto-updating code or deserializing objects without cryptographic verification.
9. **Security Logging and Monitoring Failures:** Breaches go undetected for months because login failures and critical actions are never logged.
10. **Server-Side Request Forgery (SSRF):** Tricking a backend server into making requests to internal, non-routable infrastructure (e.g. fetching cloud metadata at `http://169.254.169.254/`).

---

## 2. Daily Operational Workflows (Scoping, Testing, PoC, Remediation)

### The 5 Phases of an Engagement
1. **Scoping & Rules of Engagement (RoE):** Define target domains (e.g. `*.staging.client.com`), exclusions (do not attack production payment gateway), testing windows, and contact procedures in case of unintended service disruption.
2. **Reconnaissance & Enumeration:**
   * Passive: Searching Subdomain enumeration (`amass`, `sublist3r`), WHOIS, DNS records.
   * Active: Port scanning with **Nmap** (`nmap -sS -sV -sC target_ip`) to identify open ports, listening daemons, and software versions.
3. **Manual Web Application Testing (Proxy Interception):**
   * Route browser traffic through **Burp Suite Community Edition**.
   * Inspect all HTTP requests and responses.
   * Send interesting requests to **Burp Repeater**; manipulate parameters, headers, and payloads manually to bypass client-side validation.
4. **Authoring the Vulnerability Report:**
   * Each finding must include: **Title**, **Severity** (Critical, High, Medium, Low), **CVSS v3.1 Vector String**, **Vulnerability Description**, **Step-by-Step Proof of Concept (PoC)** with screenshots, **Business Impact**, and **Actionable Developer Remediation Guidance**.
5. **Re-Testing & Closure:**
   * After the engineering team deploys code fixes, the tester re-runs the exploit to verify that the vulnerability is cleanly patched before issuing the final closure attestation.

---

## 3. Dedicated Hands-On Lab Blueprint (Windows 11 | Local Vulnerable App)

You can run this offensive testing lab entirely locally on your Windows 11 machine without attacking external websites or needing router access.

### Architecture
* **Target:** **OWASP Juice Shop** (the most modern and sophisticated intentionally vulnerable web application, built with Node.js, Express, and Angular).
* **Interception Proxy:** **Burp Suite Community Edition** running on Windows 11.
* **Practice Platform (Free):** **PortSwigger Web Security Academy** (100% free online labs created by the makers of Burp Suite).

```
[ Web Browser (Firefox / Chrome) ]
                 │
                 │ HTTP/S Traffic Routed Through Local Proxy (127.0.0.1:8080)
                 ▼
[ Burp Suite Community Edition (Interception & Parameter Tampering) ]
                 │
                 │ Forwarded Request
                 ▼
[ OWASP Juice Shop (Running Locally on http://localhost:3000) ]
```

---

### Step-by-Step Lab Implementation

#### Exercise 1: Run OWASP Juice Shop Locally on Windows 11
You can run Juice Shop using Docker Desktop or directly via Node.js (free and lightweight):
1. Install Node.js on Windows 11 from `nodejs.org`.
2. Open PowerShell and run:
   ```powershell
   git clone https://github.com/juice-shop/juice-shop.git
   cd juice-shop
   npm install
   npm start
   ```
3. Open your browser and navigate to `http://localhost:3000`. You now have a live, deliberately vulnerable e-commerce web application running completely offline.

#### Exercise 2: Configure Burp Suite Community Edition
1. Download and install **Burp Suite Community Edition** from PortSwigger (`portswigger.net`).
2. Launch Burp Suite and use the **built-in Chromium browser** (Proxy ➔ Open browser). This requires zero manual proxy or SSL certificate setup!
3. Navigate to `http://localhost:3000` in Burp's browser.
4. Turn **Intercept On** under the Proxy tab; observe how Burp captures raw HTTP requests before they reach the Juice Shop server.

#### Exercise 3: Exploit SQL Injection (Authentication Bypass)
1. In Juice Shop, click **Login**.
2. In the Email field, enter:
   ```text
   ' or 1=1--
   ```
3. In the Password field, enter any random password (e.g. `test1234`).
4. Click **Log in**.
5. **The Concept:** The backend SQL query evaluates:
   ```sql
   SELECT * FROM Users WHERE email = '' or 1=1--' AND password = '...';
   ```
   Because `1=1` is always true and `--` comments out the rest of the password check, you are immediately logged in as the first user in the database: **the Administrator!**

#### Exercise 4: Exploit Broken Access Control (Viewing Confidential Customer Feedback)
1. In Burp Suite, inspect the HTTP traffic when viewing customer reviews.
2. Observe API requests hitting `/rest/user/whoami` or `/api/Feedbacks`.
3. Send the request to **Burp Repeater** (`Ctrl + R`).
4. Modify the request method or delete parameters to view all raw customer feedback, including internal admin comments that are hidden from the frontend UI.

#### Exercise 5: Complete PortSwigger Web Security Academy (Apprentice Tracks)
Create a free account on `portswigger.net/web-security` and complete the free interactive labs:
* **Lab 1:** SQL injection vulnerability in WHERE clause allowing retrieval of hidden data.
* **Lab 2:** Stored XSS into HTML context with nothing encoded.
* **Lab 3:** User ID controlled by request parameter (IDOR).

---

## 4. Seniority Level Progression & Career Ladder

```
┌────────────────────────────────────────────────────────────────────────┐
│ ENTRY LEVEL: Junior VAPT Analyst / Associate Security Tester (0–2 Yrs) │
│ Focus: Automated vulnerability scanning, OWASP Top 10 verification,   │
│ Burp Suite proxy testing, authoring detailed reproduction steps        │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Manual exploit chains, business logic
┌───────────────────────────────────▼────────────────────────────────────┐
│ MID LEVEL: Penetration Tester / Application Security Engineer (2–5 Yrs)│
│ Focus: Complex manual exploitation, API testing, source code review,   │
│ Active Directory domain testing, developer remediation consulting      │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Red teaming, advanced evasion, lead
┌───────────────────────────────────▼────────────────────────────────────┐
│ SENIOR LEVEL: Red Team Lead / Principal Pentest Consultant (5–8 Yrs)   │
│ Focus: Adversary simulation (C2 infrastructure), physical & social     │
│ engineering, scoping complex enterprise scopes, mentoring testers      │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │ Practice growth, CISO alignment
┌───────────────────────────────────▼────────────────────────────────────┐
│ LEADERSHIP TIER: Head of Offensive Security / Director of VAPT (8+ Yrs)│
│ Focus: Offensive security strategy, client acquisition, practice lead  │
└────────────────────────────────────────────────────────────────────────┘
```

### Detailed Breakdown by Seniority Level

#### Tier 1: Junior VAPT Analyst (Entry Level | 0–2 Years)
* **Core Responsibilities:**
  * Run automated web and network vulnerability scanners (Nessus, OpenVAS, Burp Active Scanner).
  * Manually test web applications for OWASP Top 10 flaws (SQLi, XSS, CSRF, IDOR).
  * Filter out scanner false positives by manually reproducing vulnerabilities.
  * Draft finding descriptions, CVSS scores, and reproduction steps for client reports.
* **Key Skills & Tools:** Burp Suite Community, OWASP ZAP, Nmap, Nikto, manual HTTP parameter tampering, CVSS v3.1 calculator, JIRA.
* **Indian Compensation:** **₹4.0 LPA – ₹7.5 LPA** (Boutiques: Sequretek, Kratikal, Certcube, Astra Security, Network Intelligence India).
* **How to Advance to Tier 2:** Move beyond scanner-assisted testing. Master business logic flaws, learn mobile application security (MobSF, Android APK decompilation), and master API security testing (Postman, REST/GraphQL).

#### Tier 2: Penetration Tester / AppSec Engineer (Mid Level | 2–5 Years)
* **Core Responsibilities:**
  * Conduct in-depth manual penetration tests on complex single-page apps, mobile apps, and microservice APIs.
  * Chain multiple low-severity issues into high-impact exploits (e.g. CORS misconfiguration + XSS ➔ session hijacking).
  * Conduct internal network penetration testing and Active Directory privilege escalation.
  * Perform Static Application Security Testing (SAST) and manual secure source code reviews.
* **Key Skills & Tools:** Burp Suite Professional, Metasploit, Postman, SQLMap, MobSF, BloodHound, Impacket, Python/Bash scripting.
* **Indian Compensation:** **₹9.0 LPA – ₹18.0 LPA**.
* **How to Advance to Tier 3:** Master Red Teaming (evading modern EDR solutions, building custom Command and Control (C2) infrastructure, executing Kerberoasting and Pass-the-Hash attacks).

#### Tier 3: Red Team Lead / Principal Pentest Consultant (Senior Level | 5–8 Years)
* **Core Responsibilities:**
  * Lead end-to-end Adversary Simulation (Red Team) campaigns mimicking advanced persistent threats (APTs).
  * Build custom attack tooling and bypass perimeter defenses (WAFs, modern EDRs).
  * Present executive summaries of security posture to CISOs and Engineering Vice Presidents.
* **Key Skills & Tools:** Cobalt Strike / Mythic C2, advanced Active Directory exploitation, process injection, custom payload obfuscation.
* **Indian Compensation:** **₹20.0 LPA – ₹38.0 LPA**.

#### Tier 4: Head of Offensive Security / Director of VAPT (Leadership | 8–12+ Years)
* **Core Responsibilities:**
  * Lead the offensive security practice, managing revenue, testing delivery, and client relationships.
  * Coordinate responsible disclosure programs and enterprise Bug Bounty programs.
* **Indian Compensation:** **₹45.0 LPA – ₹80+ LPA**.

---

## 5. Certification Roadmap (General & Specialization-Specific)

### General Baseline Certifications
* **Google Cybersecurity Certificate** (Coursera) – Free via financial aid. Introduces network protocols and basic packet inspection.
* **CompTIA Security+ (SY0-701)** – **₹32,000 – ₹35,000 INR**. Universal entry baseline for enterprise IT.

### VAPT & Offensive Specialization Certifications
| Certification | Issuing Body | Approx Cost (INR) | Value & Perception in India | Target Seniority |
| :--- | :--- | :--- | :--- | :--- |
| **Certified AppSec Practitioner (CAP)** | The SecOps Group | **₹8,000 – ₹12,000** | Affordable, practical entry-level validation of web application security skills. | Entry (0–2 yrs) |
| **eJPTv2 (Junior Penetration Tester)** | INE Security | **₹20,500** ($249 USD) | 100% hands-on dynamic lab exam. Proves practical network and web enumeration capability over multiple-choice tests. | Entry to Mid (1–3 yrs) |
| **Burp Suite Certified Practitioner (BSCP)** | PortSwigger | **₹8,200** ($99 USD) | Rigorous hands-on web application exploitation exam using Burp Suite Pro. Highly respected by AppSec leads. | Mid-Level (2–4 yrs) |
| **Certified Red Team Professional (CRTP)** | Altered Security | **₹20,000 – ₹25,000** | Hands-on Active Directory attack and privilege escalation exam. | Mid to Senior (2–5 yrs) |
| **OSCP (Offensive Security Certified Professional)** | OffSec | **₹1,25,000 – ₹1,45,000** | The global gold standard for penetration testing. Opens senior doors immediately in India. | Senior / Red Team (3–6 yrs) |

---

## Free Learning Resources for VAPT
* **PortSwigger Web Security Academy:** The world's best free web security training platform (`portswigger.net/web-security`).
* **OWASP Juice Shop:** Deliberately vulnerable modern web application (`pwning.owasp-juice.shop`).
* **OverTheWire Bandit:** Hands-on Linux command line and privilege exploration wargame (`overthewire.org`).
