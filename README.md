# The Complete Cybersecurity Career Roadmap: Entry Pathways, Learning Blueprint & Pay Structure (India 2026)

[![Status](https://img.shields.io/badge/Status-Complete%20Master%20Roadmap-brightgreen.svg)](#)
[![Market](https://img.shields.io/badge/Market-India%20(IT%20Services%20%7C%20GCCs%20%7C%20Boutiques%20%7C%20Startups)-orange.svg)](#)
[![Approach](https://img.shields.io/badge/Architecture-General%20Concepts%20%3E%20Job--Specific%20Concepts-blue.svg)](#)
[![Data Source](https://img.shields.io/badge/Verified-2026%20Indian%20Compensation%20Data-purple.svg)](#)

A structured, battle-tested career transition roadmap designed for **designers and non-technical professionals** to systematically move into cybersecurity in India. This roadmap establishes universal foundations first, branches into the **most-hired entry-level job roles in India**, outlines clear technical requirements, and details future career progression with verified Indian pay structures.

---

## Master Architecture & Specialization Modules

```
┌────────────────────────────────────────────────────────────────────────┐
│                   PHASE 1: UNIVERSAL CORE FOUNDATIONS                  │
│       (Systems Internals ➔ Networking Protocols ➔ Core Security)      │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
    ┌───────────────────────────────┼───────────────────────────────┐
    │                               │                               │
┌───▼──────────────┐       ┌────────▼─────────┐            ┌────────▼─────────┐
│ PATHWAY 1:       │       │ PATHWAY 2:       │            │ PATHWAY 3:       │
│ SOC Analyst L1   │       │ IAM Operations   │            │ GRC & Privacy    │
│ (Incident Triage)│       │ (Access Control) │            │ (DPDP / Audit)   │
└───┬──────────────┘       └────────┬─────────┘            └────────┬─────────┘
    │                               │                               │
    ├───────────────────────────────┼───────────────────────────────┤
    │                               │                               │
┌───▼──────────────┐       ┌────────▼─────────┐            ┌────────▼─────────┐
│ PATHWAY 4:       │       │ PATHWAY 5:       │            │ PATHWAY 6 & 7:   │
│ Junior VAPT      │       │ Cloud Security   │            │ IT Support / QA  │
│ (Offensive Web)  │       │ Associate        │            │ Stepping Stones  │
└───┬──────────────┘       └────────┬─────────┘            └────────┬─────────┘
    │                               │                               │
    └───────────────────────────────┴───────────────────────────────┘
                                    │
┌───────────────────────────────────▼────────────────────────────────────┐
│                    PHASE 3: SENIOR & LEADERSHIP TIERS                  │
│  (Incident Response Lead ➔ Security Architect ➔ Principal ➔ CISO)      │
└────────────────────────────────────────────────────────────────────────┘
```

### Specialized Deep-Dive Guides (Dedicated Manuals)
* 🧭 **[Choosing Your Track & Compensation Analysis](TRACK_SELECTION_AND_PAY_ANALYSIS.md)**: How to choose which track suits your work style and diagnostic profile, plus detailed 2026 Indian pay ceilings.
* 📘 **[SOC & Incident Response Deep Dive](SOC_AND_INCIDENT_RESPONSE.md)**: Telemetry pipelines, SIEM correlation, Wazuh + Sysmon local lab, L1 to CISO career progression, and SOC certifications.
* 🔑 **[IAM & Identity Security Deep Dive](IAM_IDENTITY_ACCESS_MANAGEMENT.md)**: Active Directory, Kerberos/SAML/OIDC, JML lifecycles, Windows Server 2022 AD lab, and IAM career progression.
* ⚖️ **[GRC & Data Privacy (DPDP Act 2023) Deep Dive](GRC_PRIVACY_COMPLIANCE.md)**: ISO 27001 auditing, India DPDP Act 2023 compliance, RoPA registers, non-conformities, and DPO career progression.
* 🎯 **[VAPT & Application Security Deep Dive](VAPT_APPLICATION_SECURITY.md)**: OWASP Top 10, local OWASP Juice Shop + Burp Suite lab, manual parameter tampering, and Pentest career progression.
* ☁️ **[Cloud Security & DevSecOps Deep Dive](CLOUD_SECURITY_DEVSECOPS.md)**: Shared Responsibility Model, Cloud IAM JSON policies, local Checkov IaC security scanning, and Cloud Architect progression.
* 🎙️ **[Interview Master Playbook](INTERVIEW_MASTER_PLAYBOOK.md)**: Word-for-word scripts for the 6 technical interview scenarios that screen candidates out.

---

## Table of Contents
1. [Phase 1: Universal Core Foundations (General Concepts)](#1-phase-1-universal-core-foundations-general-concepts)
2. [Market Research: Most-Hired Entry-Level Cybersecurity Roles in India](#2-market-research-most-hired-entry-level-cybersecurity-roles-in-india)
3. [Pathway 1: Security Operations Center (SOC) Analyst L1](#3-pathway-1-security-operations-center-soc-analyst-l1)
4. [Pathway 2: Identity & Access Management (IAM) Operations Analyst](#4-pathway-2-identity--access-management-iam-operations-analyst)
5. [Pathway 3: GRC Analyst & Data Privacy Analyst (DPDP Act 2023)](#5-pathway-3-grc-analyst--data-privacy-analyst-dpdp-act-2023)
6. [Pathway 4: Junior VAPT Analyst (Vulnerability Assessment & Pentesting)](#6-pathway-4-junior-vapt-analyst-vulnerability-assessment--pentesting)
7. [Pathway 5: Cloud Security Associate (AWS / Azure)](#7-pathway-5-cloud-security-associate-aws--azure)
8. [Pathway 6: IT Support / Systems Administrator (Gateway to SecOps)](#8-pathway-6-it-support--systems-administrator-gateway-to-secops)
9. [Pathway 7: Software QA / Manual Tester (Gateway to AppSec)](#9-pathway-7-software-qa--manual-tester-gateway-to-appsec)
10. [Master Pay Structure & Career Progression Matrix (India 2026)](#10-master-pay-structure--career-progression-matrix-india-2026)
11. [General & Specialization Certification Master Matrix](#11-general--specialization-certification-master-matrix)
12. [Universal Hands-On Lab Architecture (Zero Router Access Needed)](#12-universal-hands-on-lab-architecture-zero-router-access-needed)
13. [16-Week Concrete Execution Schedule](#13-16-week-concrete-execution-schedule)

---

## 1. Phase 1: Universal Core Foundations (General Concepts)

Every cybersecurity role relies on the same three underlying disciplines: **Operating Systems**, **Networking**, and **Core Security Architecture**. 

You must master these universal foundations before touching specialized tools.

```
┌────────────────────────────────────────────────────────┐
│ Module 1: Computer Systems & Operating System Internals│
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Module 2: Computer Networking & Internet Protocols     │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Module 3: Security Architecture & Cryptography Basics  │
└────────────────────────────────────────────────────────┘
```

### Module 1: Computer Systems & OS Internals
* **The OS Kernel & User Space:** How an operating system manages processes, RAM memory allocations, and hardware abstraction.
* **Windows Internals:**
  * File System Security: NTFS permissions (Read, Write, Execute, Modify, Full Control) and Access Control Lists (ACLs).
  * System Components: Windows Registry hives (`HKLM`, `HKCU`), Windows Services (`services.msc`), Task Scheduler.
  * Audit Logging: Windows Event Log architecture (`Application`, `System`, `Security`).
* **Linux Essentials (Ubuntu / Fedora / Debian):**
  * POSIX File Permissions: Owner, Group, Others (`rwx`, `chmod`, `chown`, numeric values `755`, `770`, `600`).
  * Process Management: Process IDs (`PID`), `ps aux`, `top`/`htop`, `kill`.
  * CLI Text Manipulation: `cat`, `grep`, `awk`, `sed`, `find`, `tail -f`, piping (`|`).
  * Systemd & Logs: `systemctl`, `journalctl`, `/var/log/auth.log` or `/var/log/secure`.

### Module 2: Computer Networking & Internet Protocols
* **The Communication Models:**
  * The OSI 7-Layer Model: Physical ➔ Data Link ➔ Network ➔ Transport ➔ Session ➔ Presentation ➔ Application.
  * The TCP/IP Model: Network Interface ➔ Internet ➔ Transport ➔ Application. Data encapsulation (Frame ➔ Packet ➔ Segment ➔ Data).
* **Addressing & Subnetting:**
  * Layer 2: MAC addresses and Address Resolution Protocol (ARP).
  * Layer 3: IPv4 Private subnets (RFC 1918: `10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`), subnet masks, CIDR notation (`/24`), default gateways, and loopback (`127.0.0.1`).
* **Transport Protocols:**
  * **TCP:** Connection-oriented, reliable. The 3-way handshake (`SYN ➔ SYN-ACK ➔ ACK`) and session termination (`FIN / RST`).
  * **UDP:** Connectionless, lightweight (DNS, DHCP, streaming).
* **Core Application Protocols & Common Ports:**
  * **Port 53 (DNS):** Resolution hierarchy (Root ➔ TLD ➔ Authoritative nameservers); record types (`A`, `AAAA`, `CNAME`, `MX`, `TXT`, `PTR`).
  * **Port 67/68 (DHCP):** DORA process (Discover, Offer, Request, Acknowledge).
  * **Port 80/443 (HTTP/HTTPS):** Request/Response headers, methods (`GET`, `POST`, `PUT`, `DELETE`), status codes (2xx, 3xx, 4xx, 5xx), cookies (`SameSite`, `HttpOnly`, `Secure`), TLS 1.3 cryptographic handshake.
  * **Administrative Ports:** Port 22 (SSH), Port 3389 (RDP), Port 445 (SMB), Port 389/636 (LDAP/LDAPS).

### Module 3: Security Architecture & Cryptography Basics
* **The CIA Triad:**
  * *Confidentiality:* Data is accessible only to authorized entities (AES-256 encryption, TLS).
  * *Integrity:* Data is not altered undetected (cryptographic hashing: SHA-256).
  * *Availability:* Systems remain operational (redundancy, backups, DDoS mitigation).
* **The AAA Framework:**
  * *Authentication (AuthN):* Proving identity (Passwords, Passkeys/FIDO2, TOTP, Push, Biometrics).
  * *Authorization (AuthZ):* Granting specific permissions (RBAC, Principle of Least Privilege).
  * *Accounting:* Auditing system activities (logging who did what and when).
* **Core Cryptography:**
  * Hashing vs. Encryption vs. Encoding: Hashing is one-way (SHA-256); encryption is reversible with a key (AES); encoding is data formatting without security (Base64).
  * Asymmetric Cryptography: Public/Private keypair mechanics (RSA, ECC, Ed25519) for digital signatures and key exchange.
* **Threat Modeling:** The STRIDE framework (**S**poofing, **T**ampering, **R**epudiation, **I**nformation Disclosure, **D**enial of Service, **E**levation of Privilege).

---

## 2. Market Research: Most-Hired Entry-Level Cybersecurity Roles in India

Based on 2026 hiring data across Indian IT service giants, Global Capability Centers (GCCs in Bengaluru, Hyderabad, Pune, Gurugram), boutique Managed Security Service Providers (MSSPs), and product tech startups:

```
┌────────────────────────────────────────────────────────────────────────┐
│               MOST HIRED ENTRY-LEVEL CYBERSECURITY ROLES               │
│                                                                        │
│ 1. SOC Analyst L1 (Highest Hiring Volume in India)                     │
│ 2. IAM Operations Analyst (Fastest-Growing Operational Demand)         │
│ 3. GRC Analyst / DPDP Privacy Associate (Surging Regulatory Demand)    │
│ 4. Junior VAPT / Web Pentester (High Demand in Cyber Boutiques)        │
│ 5. Cloud Security Associate (High Demand in Enterprise & SaaS)         │
│ 6. IT Support / SysAdmin (The Battle-Tested Operational Gateway)       │
│ 7. Software QA / Manual Tester (The Software & Logic Gateway)          │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Pathway 1: Security Operations Center (SOC) Analyst L1

### Role Overview
The **SOC Analyst L1** is the front-line defender in an enterprise or MSSP. The analyst monitors security information and event management (SIEM) consoles, triages incoming alerts, investigates anomalies, validates True Positives vs. False Positives, and escalates confirmed threats to Tier-2 incident responders.

* **Job-Specific Concepts to Learn:** SIEM query syntax (Splunk, Wazuh, Sentinel), Windows Security Event IDs (4624, 4625, 4688, 4728) + Logon Types (2, 3, 10), Sysmon process tree triage (Event ID 1, 3), RFC 822 email header phishing analysis (SPF, DKIM, DMARC), and NIST SP 800-61 incident containment.
* **Future Progression:** L1 SOC Analyst ➔ L2/L3 Incident Responder / Threat Hunter ➔ SOC Lead / IR Manager ➔ Head of Cyber Defense / CISO.
* **Pay Structure in India:** Entry: **₹3.5–6.5 LPA** | Mid: **₹8.0–14.0 LPA** | Senior: **₹16.0–28.0 LPA** | Leadership: **₹35.0–60+ LPA**.
* 📖 **Full Operational Manual:** See **[SOC_AND_INCIDENT_RESPONSE.md](SOC_AND_INCIDENT_RESPONSE.md)**.

---

## 4. Pathway 2: Identity & Access Management (IAM) Operations Analyst

### Role Overview
The **IAM Operations Analyst** governs digital identities across the enterprise. The analyst manages user lifecycles, ensures access adheres to the Principle of Least Privilege, provisions and deprovisions permissions, supports Single Sign-On (SSO) integrations, and prepares audit-ready access reports.

* **Job-Specific Concepts to Learn:** Active Directory Domain Services (AD DS), Microsoft Entra ID (Azure AD), Joiner-Mover-Leaver (JML) lifecycle, Role-Based Access Control (RBAC), SSO protocols (SAML 2.0, OpenID Connect), OAuth 2.0 authorization grants, and Privileged Access Management (PAM).
* **Future Progression:** IAM Operations Analyst ➔ IAM Engineer / SailPoint Specialist ➔ Senior IAM Architect ➔ Director of Identity Security / CISO.
* **Pay Structure in India:** Entry: **₹4.5–7.5 LPA** | Mid: **₹9.0–16.0 LPA** | Senior: **₹18.0–30.0 LPA** | Leadership: **₹35.0–55+ LPA**.
* 📖 **Full Operational Manual:** See **[IAM_IDENTITY_ACCESS_MANAGEMENT.md](IAM_IDENTITY_ACCESS_MANAGEMENT.md)**.

---

## 5. Pathway 3: GRC Analyst & Data Privacy Analyst (DPDP Act 2023)

### Role Overview
The **GRC Analyst** evaluates information security policies against legal and regulatory standards. With India's **Digital Personal Data Protection (DPDP) Act 2023** now in enforcement, demand has surged for professionals who assess data flows, manage user consent mechanisms, audit third-party vendors, and coordinate security awareness. **Zero coding required.**

* **Job-Specific Concepts to Learn:** ISO/IEC 27001:2022 clauses and Annex A controls, India DPDP Act 2023 (Sections 5, 6, 9, 11–13: Notice, Consent Managers, Data Principal Rights), NIST CSF 2.0, SOC 2 Type II criteria, Third-Party Risk Management (TPRM), and RoPA registers.
* **Future Progression:** GRC / Privacy Analyst ➔ GRC / Privacy Consultant ➔ GRC Lead / Data Protection Officer (DPO) ➔ Chief Risk Officer (CRO) / CISO.
* **Pay Structure in India:** Entry: **₹4.5–7.5 LPA** | Mid: **₹10.0–18.0 LPA** | Senior: **₹20.0–36.0 LPA** | Leadership: **₹40.0–75+ LPA**.
* 📖 **Full Operational Manual:** See **[GRC_PRIVACY_COMPLIANCE.md](GRC_PRIVACY_COMPLIANCE.md)**.

---

## 6. Pathway 4: Junior VAPT Analyst (Vulnerability Assessment & Pentesting)

### Role Overview
The **Junior VAPT Analyst** discovers and exploits security vulnerabilities in web applications, network infrastructure, and APIs. The analyst runs automated vulnerability scanners, conducts manual penetration tests, verifies exploits, and authors remediation reports for software engineering teams.

* **Job-Specific Concepts to Learn:** OWASP Top 10 (SQLi, XSS, Broken Access Control / IDOR, SSRF), Burp Suite Community Edition (Proxy, Repeater, Intruder), Nmap reconnaissance, CVSS v3.1 scoring, and developer remediation reporting.
* **Future Progression:** Junior VAPT Analyst ➔ Penetration Tester / Red Team Operator ➔ Senior Red Team Lead / Principal Pentester ➔ Head of Offensive Security.
* **Pay Structure in India:** Entry: **₹4.0–7.5 LPA** | Mid: **₹9.0–18.0 LPA** | Senior: **₹20.0–38.0 LPA** | Leadership: **₹45.0–80+ LPA**.
* 📖 **Full Operational Manual:** See **[VAPT_APPLICATION_SECURITY.md](VAPT_APPLICATION_SECURITY.md)**.

---

## 7. Pathway 5: Cloud Security Associate (AWS / Azure)

### Role Overview
The **Cloud Security Associate** monitors and configures cloud infrastructure to prevent misconfigurations, unauthorized access, and data leaks. The associate implements cloud identity policies, audits storage buckets, inspects network security groups, and analyzes cloud control-plane logs.

* **Job-Specific Concepts to Learn:** Cloud Shared Responsibility Model, VPCs, subnets, AWS IAM JSON policies, Azure RBAC, S3 bucket permission auditing, Security Group hardening, CloudTrail / Activity logging, and Infrastructure-as-Code (IaC) scanning with Checkov.
* **Future Progression:** Cloud Operations Security Associate ➔ Cloud Security Engineer / DevSecOps ➔ Senior Cloud Security Architect ➔ VP of Cloud Security.
* **Pay Structure in India:** Entry: **₹5.0–9.0 LPA** | Mid: **₹12.0–22.0 LPA** | Senior: **₹25.0–48.0 LPA** | Leadership: **₹50.0–90+ LPA**.
* 📖 **Full Operational Manual:** See **[CLOUD_SECURITY_DEVSECOPS.md](CLOUD_SECURITY_DEVSECOPS.md)**.

---

## 8. Pathway 6: IT Support / Systems Administrator (Gateway to SecOps)

### Role Overview
The **IT Support / Systems Administrator** role is the most reliable stepping-stone into tech operations in India. It accepts candidates from all academic backgrounds, places them directly on an enterprise IT payroll, and provides daily hands-on exposure to endpoints, networking, identity, and access controls.

* **Job-Specific Concepts to Learn:** Endpoint troubleshooting (Windows, Linux, macOS), Active Directory password resets and account provisioning, network diagnostics (`ipconfig`, `ping`, `tracert`, `nslookup`), antivirus and patch deployment, and ITSM ticketing (ServiceNow, JIRA).
* **The 12-Month IJP Pivot:** Work 6–9 months on the support desk ➔ volunteer with internal InfoSec on security tasks ➔ apply internally via **Internal Job Posting (IJP)** to the SOC, IAM, or Endpoint Security team without external ATS degree filtering.
* **Pay Structure in India:** Support Entry: **₹3.0–4.8 LPA** | SysAdmin / Cyber Transition: **₹6.0–11.0 LPA** | SecOps Lead: **₹14.0–24.0 LPA** | Leadership: **₹25.0–45+ LPA**.

---

## 9. Pathway 7: Software QA / Manual Tester (Gateway to AppSec)

### Role Overview
The **Software QA Tester** ensures software functions correctly before production release. Because software testing involves analyzing user workflows, input edge cases, and unexpected system behaviors, it is the direct conceptual sibling to **Application Security (AppSec) and VAPT**.

* **Job-Specific Concepts to Learn:** Test case authoring, boundary value analysis, regression testing, inspecting HTTP traffic and DOM elements in browser Developer Tools, parameter tampering, and negative input testing using Burp Suite.
* **The Progression:** Manual QA Tester ➔ Security QA Tester / Associate VAPT Analyst ➔ Application Security (AppSec) Engineer ➔ Head of Product Security.
* **Pay Structure in India:** QA Entry: **₹3.2–5.0 LPA** | Security QA / VAPT: **₹7.0–13.0 LPA** | Senior AppSec: **₹16.0–32.0 LPA** | Leadership: **₹35.0–65+ LPA**.

---

## 10. Master Pay Structure & Career Progression Matrix (India 2026)

| Specialization Track | Entry Role (0–2 Years) | Mid-Level Role (3–5 Years) | Senior Role (6–10 Years) | Leadership Role (10+ Years) |
| :--- | :--- | :--- | :--- | :--- |
| **SOC & Blue Team Defense** | **L1 SOC Analyst**<br>₹3.5 – 6.5 LPA | **L2/L3 Incident Responder**<br>₹8.0 – 14.0 LPA | **SOC Lead / Threat Hunter**<br>₹16.0 – 28.0 LPA | **SOC Manager / CISO**<br>₹35.0 – 60+ LPA |
| **Identity & Access (IAM)** | **IAM Operations Analyst**<br>₹4.5 – 7.5 LPA | **IAM Engineer / SailPoint**<br>₹9.0 – 16.0 LPA | **Senior IAM Architect**<br>₹18.0 – 30.0 LPA | **Director of IAM / CISO**<br>₹35.0 – 55+ LPA |
| **GRC & Privacy (DPDP)** | **GRC / Privacy Analyst**<br>₹4.5 – 7.5 LPA | **Privacy / GRC Consultant**<br>₹10.0 – 18.0 LPA | **GRC Lead / DPO**<br>₹20.0 – 36.0 LPA | **Chief Risk Officer / CISO**<br>₹40.0 – 75+ LPA |
| **Offensive Security (VAPT)** | **Junior VAPT Analyst**<br>₹4.0 – 7.5 LPA | **Penetration Tester**<br>₹9.0 – 18.0 LPA | **Senior Red Team Lead**<br>₹20.0 – 38.0 LPA | **Head of Offensive Sec**<br>₹45.0 – 80+ LPA |
| **Cloud Security & DevSecOps** | **Cloud Security Associate**<br>₹5.0 – 9.0 LPA | **Cloud Security Engineer**<br>₹12.0 – 22.0 LPA | **Cloud Security Architect**<br>₹25.0 – 48.0 LPA | **VP of Cloud Security**<br>₹50.0 – 90+ LPA |
| **IT Support Gateway** | **Desktop Support Engineer**<br>₹3.0 – 4.8 LPA | **SysAdmin ➔ Cyber Pivot**<br>₹6.0 – 11.0 LPA | **SecOps Engineer**<br>₹14.0 – 24.0 LPA | **Infrastructure Director**<br>₹25.0 – 45+ LPA |
| **QA / Testing Gateway** | **Manual QA Tester**<br>₹3.2 – 5.0 LPA | **Security QA / AppSec**<br>₹7.0 – 13.0 LPA | **Senior AppSec Engineer**<br>₹16.0 – 32.0 LPA | **Head of Product Security**<br>₹35.0 – 65+ LPA |

---

## 11. General & Specialization Certification Master Matrix

A realistic, transparent breakdown of certifications in India, separating universal baseline credentials from specialized career certs:

### A. General Baseline Certifications (Foundational Across All Cyber Roles)
| Certification | Provider | Official Cost (INR / USD) | Indian Market ROI & Value | Free Study Alternative |
| :--- | :--- | :--- | :--- | :--- |
| **Google Cybersecurity Certificate** | Google / Coursera | **₹0** (via Financial Aid) or Coursera sub | Excellent beginner orientation; covers Linux, SQL, SIEM, Python. | Audit all courses for free on Coursera |
| **ISC2 Certified in Cybersecurity (CC)** | ISC2 | **₹0 – ₹4,200** ($50 AMF fee) | Globally recognized entry-level credential from ISC2. Free training online. | Official ISC2 free self-paced course |
| **Microsoft SC-900 (Security Fundamentals)** | Microsoft | **₹4,800 INR** ($99 USD) | High recognition in corporate IT; covers Microsoft security and Entra ID. | Complete Microsoft Learn SC-900 modules |
| **CompTIA Security+ (SY0-701)** | CompTIA | **₹32,000 – ₹35,000 INR** ($404 USD) | The universal entry-level hiring benchmark across Indian MNCs and GCCs. | Professor Messer free YouTube video course |

### B. Specialization-Specific Certifications Matrix
| Track | Entry / Associate Level (0–2 Yrs) | Mid-Level / Professional (2–5 Yrs) | Senior / Architectural (5+ Yrs) |
| :--- | :--- | :--- | :--- |
| **SOC & Incident Response** | **Microsoft SC-200** (~₹4,800 INR)<br>• Sentinel KQL & Defender XDR<br><br>**Blue Team Level 1 (BTL1)** (~₹42,000 INR)<br>• 24-hr hands-on incident response | **CompTIA CySA+** (~₹34,000 INR)<br>• Threat detection & analysis<br><br>**Certified SOC Analyst (CSA)** (~₹30,000 INR) | **GIAC Certified Incident Handler (GCIH)** (~₹1,20,000+ INR)<br><br>**CISSP** (~₹65,000 INR) |
| **Identity & Access (IAM)** | **Microsoft SC-300** (~₹4,800 INR)<br>• Entra ID, PIM, Conditional Access | **Okta Certified Administrator** (~₹20,500 INR)<br><br>**SailPoint Certified IdentityIQ Associate** (~₹30,000 INR) | **CyberArk Certified Defender** (~₹25,000 INR)<br><br>**CISM / CISSP** (~₹55,000–65,000 INR) |
| **GRC & Data Privacy** | **ISO/IEC 27001:2022 Lead Auditor** (~₹26,000–36,000 INR)<br>• Gold standard for Big 4 / IT GRC<br><br>**DSCI DCDPO** (~₹28,000 INR)<br>• India DPDP Act compliance | **IAPP CIPP/E** (~₹45,000 INR)<br>• Global GDPR privacy benchmark<br><br>**IAPP CIPM** (~₹45,000 INR)<br>• Privacy program management | **ISACA CISA** (~₹50,000 INR)<br>• Information systems auditing<br><br>**ISACA CRISC** (~₹50,000 INR)<br>• Enterprise risk management |
| **VAPT & Offensive Security** | **Certified AppSec Practitioner (CAP)** (~₹10,000 INR)<br>• Entry web application security<br><br>**eJPTv2** (~₹20,500 INR / $249 USD)<br>• 48-hr hands-on network/web lab | **Burp Suite Certified Practitioner (BSCP)** (~₹8,200 INR)<br>• Real-world web application exploitation<br><br>**CRTP** (~₹22,000 INR)<br>• Active Directory red teaming | **OSCP** (~₹1,35,000 INR)<br>• Hands-on 24-hour penetration test gold standard<br><br>**OSWE** (~₹1,35,000 INR)<br>• Web application exploitation |
| **Cloud Security & DevSecOps** | **AWS Cloud Practitioner (CLF-C02)** (~₹8,200 INR)<br><br>**Microsoft AZ-900 / SC-900** (~₹4,800 INR) | **Microsoft AZ-500** (~₹4,800 INR)<br>• Azure Security Technologies<br><br>**AWS Certified Security - Specialty** (~₹24,500 INR) | **CCSP (Certified Cloud Security Professional)** (~₹50,000 INR)<br><br>**CISSP** (~₹65,000 INR) |

---

## 12. Universal Hands-On Lab Architecture (Zero Router Access Needed)

To prove practical competence during technical scenario interviews, you do **not** need access to your physical Wi-Fi router. Modern hypervisors (**VMware Workstation Pro** or **Oracle VirtualBox**) create software-defined virtual switches inside your computer:
* **Host-Only Virtual Network:** An internal virtual switch running in your PC's memory. VMs on this switch can only talk to each other and your host machine. No traffic leaves your computer, making it 100% safe, legal, and isolated from your home network.

```
       [ Windows 11 Host PC (Your Machine) ]
                         │
          ┌──────────────┴──────────────┐
          │ Hypervisor Virtual Switch    │
          │ (Host-Only Network: vmnet1) │
          └──────┬──────────────┬───────┘
                 │              │
      ┌──────────▼────────┐   ┌─▼─────────────────┐
      │ Linux Fedora/     │   │ Windows Target VM │
      │ Ubuntu Server     │   │ (SMB Client /     │
      │ (SSH, Samba, NGINX│   │  Web Client)      │
      └───────────────────┘   └───────────────────┘
   * Completely isolated inside your PC — 0 router access needed.
```

### Specialized Lab Blueprints (Choose Your Track):
1. **SOC & Blue Team Lab:** Install Microsoft Sysmon (SwiftOnSecurity config) on Windows; deploy Wazuh Manager on an Ubuntu VM; simulate brute force from Kali; tune detection rules. ➔ *See [SOC_AND_INCIDENT_RESPONSE.md](SOC_AND_INCIDENT_RESPONSE.md)*
2. **IAM & Active Directory Lab:** Install Windows Server 2022 evaluation VM; promote to Domain Controller (`corp.lab`); configure OUs, RBAC groups, and GPO lockout policies; connect to a free Microsoft 365 developer tenant. ➔ *See [IAM_IDENTITY_ACCESS_MANAGEMENT.md](IAM_IDENTITY_ACCESS_MANAGEMENT.md)*
3. **GRC & Privacy Toolkit:** Author a live DPDP Act 2023 RoPA register; design a Section 5-compliant consent wireframe; build an ISO 27001 Statement of Applicability (SoA) spreadsheet. ➔ *See [GRC_PRIVACY_COMPLIANCE.md](GRC_PRIVACY_COMPLIANCE.md)*
4. **VAPT & Web Security Lab:** Run OWASP Juice Shop locally via Node.js; configure Burp Suite Community Edition proxy; exploit authentication bypass SQLi and IDOR access control bugs. ➔ *See [VAPT_APPLICATION_SECURITY.md](VAPT_APPLICATION_SECURITY.md)*
5. **Cloud Security Lab:** Install Checkov locally on Windows PowerShell; write an intentionally misconfigured Terraform file; scan and remediate cloud security flaws. ➔ *See [CLOUD_SECURITY_DEVSECOPS.md](CLOUD_SECURITY_DEVSECOPS.md)*

---

## 13. 16-Week Concrete Execution Schedule

```
Weeks 1–4: Universal Core Foundations (OS Internals, TCP/IP, Protocols, CIA Triad)
Weeks 5–8: Target Role Deep-Dive (Pick ONE: SOC, IAM, GRC, VAPT, or Cloud)
Weeks 9–12: Hands-on Lab Drills & Publishing 2 Incident Reports to GitHub
Weeks 13–16: Tailored Resume Applications (15–20/wk) & Scenario Interview Defense
```

* **Weeks 1–4 (Universal Foundations):**
  * Watch Professor Messer's CompTIA Network+ & Security+ video modules (YouTube, free).
  * Practice Linux command line basics on a local Ubuntu VM.
  * Trace HTTP headers, cookies, and TLS handshakes in browser Developer Tools.
* **Weeks 5–8 (Role Specialization):**
  * *If SOC:* Complete TryHackMe SOC Level 1 free rooms and practice Windows Event log analysis.
  * *If IAM:* Study Active Directory user lifecycle (JML), SAML/OIDC, and Microsoft Entra ID.
  * *If GRC:* Study ISO 27001 Annex A controls and India's DPDP Act 2023 official gazette.
  * *If VAPT:* Complete PortSwigger Web Security Academy free modules (SQLi, XSS, CSRF).
  * *If Cloud:* Complete AWS Skill Builder Cloud Practitioner Essentials and Microsoft Learn AZ-900.
* **Weeks 9–12 (Hands-on Proof of Work):**
  * Execute your chosen specialized local lab on Windows 11.
  * Write two detailed incident triage reports with MITRE ATT&CK mapping.
  * Publish the reports to your public GitHub repository (`github.com/<username>`).
* **Weeks 13–16 (Job Applications & Interview Execution):**
  * Tailor your resume specifically to your target entry role.
  * Apply to 15–20 openings per week on LinkedIn India, Instahyre, and Foundit.
  * Rehearse the scenario-based response framework in **[INTERVIEW_MASTER_PLAYBOOK.md](INTERVIEW_MASTER_PLAYBOOK.md)**: **Scope ➔ Enrich ➔ Contain ➔ Eradicate ➔ Document**.
