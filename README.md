# Designer to Cybersecurity: The Definitive Career Transition Roadmap (India Edition)

[![Roadmap Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)](#)
[![Target Market](https://img.shields.io/badge/Market-India%20(GCC%20%7C%20Services%20%7C%20Startups)-orange.svg)](#)
[![Cost Philosophy](https://img.shields.io/badge/Philosophy-Free--First-blue.svg)](#)
[![Lab Setup](https://img.shields.io/badge/Home%20Lab-Windows%2011%20%7C%20No%20Router%20Access%20Needed-purple.svg)](#)

A structured, realistic, and battle-tested guide for graphic, visual, UI/UX, web, and product designers transitioning into cybersecurity in India. This roadmap is designed with zero technical assumptions, prioritizes zero-cost open educational resources, provides safe local virtualization lab blueprints that require **no router access**, and analyzes hiring dynamics across Indian Global Capability Centers (GCCs), IT service giants, Big 4 consulting firms, and product startups.

---

## Table of Contents
1. [Intake & Assessment Dimensions](#1-intake--assessment-dimensions)
2. [Route Comparison Matrix & Trade-offs](#2-route-comparison-matrix--trade-offs)
3. [The Indian Cybersecurity Job Market Reality](#3-the-indian-cybersecurity-job-market-reality)
4. [Shared Foundations (Stage 0 to Stage 2)](#4-shared-foundations-stage-0-to-stage-2)
5. [No-Router Home Lab Architecture (Windows 11)](#5-no-router-home-lab-architecture-windows-11)
6. [Specialized Career Branches](#6-specialized-career-branches)
   - [Branch 1: Security UX, Human Factors & Secure Product Design](#branch-1-security-ux-human-factors--secure-product-design)
   - [Branch 2: Web & Application Security (AppSec)](#branch-2-web--application-security-appsec)
   - [Branch 3: GRC, Privacy (DPDP Act 2023) & Security Awareness](#branch-3-grc-privacy-dpdp-act-2023--security-awareness)
   - [Branch 4: Security Operations Center (SOC) & Blue Team](#branch-4-security-operations-center-soc--blue-team)
   - [Branch 5: Identity & Access Management (IAM)](#branch-5-identity--access-management-iam)
   - [Branch 6: Cloud Security](#branch-6-cloud-security)
7. [Free vs. Paid Resource Breakdown](#7-free-vs-paid-resource-breakdown)
8. [Roadmap.sh "Text to Roadmap" Formatted Code](#8-roadmapsh-text-to-roadmap-formatted-code)
9. [Portfolio, Resume & Indian Interview Preparation](#9-portfolio-resume--indian-interview-preparation)

---

## 1. Intake & Assessment Dimensions

Transitioning into cybersecurity from design is not one-size-fits-all. Your optimal path depends on 7 specific vectors:

| Parameter | Options / Categories | Strategic Impact on Cybersecurity Path |
| :--- | :--- | :--- |
| **Design Background** | UI/UX, Product Design, Web Design (HTML/CSS), Graphic/Visual/Brand | UI/UX & Product → Security UX or IAM; Web Design → AppSec/WebSec; Graphic/Visual → GRC, Awareness & Human Risk. |
| **Years of Experience** | Fresher (0-1 yr), Mid-level (2-5 yrs), Senior (5+ yrs) | Experienced designers shouldn't start at ₹3 LPA L1 SOC desks if they can leverage design seniority into Security UX, GRC advisory, or Product Security. |
| **Technical Exposure** | Zero coding, basic HTML/CSS, attempted home labs, light scripting | Influences whether to take a direct technical route (SOC/AppSec) or an adjacent human/policy route (GRC/Privacy). |
| **Formal Education** | B.Tech/BCA/MCA/B.Sc IT vs. BA/B.Des/B.Com/BBA/Non-STEM | Indian IT service HR screening filters often look for STEM degrees. Non-STEM candidates achieve higher success in GCCs, design-led security SaaS, and specialized GRC roles. |
| **Geographic Hub in India** | Bengaluru, Hyderabad, Pune, Gurugram/NCR, Chennai, Mumbai, Remote | GCCs dominate Bengaluru/Hyderabad; BFSI/Consulting dominates Mumbai/NCR; IT Services dominate Pune/Chennai. |
| **Weekly Study Bandwidth** | 5–10 hrs/week (Part-time), 15–20 hrs/week (Accelerated), 30+ hrs/week (Full-time) | Dictates transition timeline: 12–18 months vs. 6–9 months vs. 4–6 months. |
| **Preferred Work Style** | Visual & Human-centered, Systematic/Compliance, Analytical Investigation, Engineering/Code | Determines whether you will thrive under high-stress 24/7 SOC shift rotations or asynchronous threat modeling and design reviews. |

---

## 2. Route Comparison Matrix & Trade-offs

| Route | Prerequisites | Learning Curve | Indian Entry-Level Titles | Typical Entry Salary (India) | Hiring Volume in India | Key Trade-offs & Reality |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Design → Security UX / Human Factors / Secure Product Design** | Strong UI/UX fundamentals, Figma, user research, baseline security concepts (auth, warnings, friction). | Low to Medium | • Product Designer - Security<br>• UX Researcher (Identity/Privacy)<br>• Security UX Specialist | **₹8 – 16 LPA** (Product/SaaS/GCCs) | Low to Medium (Niche, highly valued) | **Pro:** Retains design mastery; high pay.<br>**Con:** Fewer total openings in India than SOC; primarily in global cyber SaaS (Palo Alto Networks, CrowdStrike, Zscaler, Cisco India) or mature FinTechs. |
| **2. Web/UI Design → Web & Application Security (AppSec)** | HTML/CSS, basic JavaScript/DOM, HTTP/S request-response model, OWASP Top 10. | High | • Junior AppSec Engineer<br>• Associate Security Analyst (VAPT)<br>• Web Security Specialist | **₹6 – 12 LPA** (Tech startups, GCCs, VAPT Boutiques) | High (Rapidly growing) | **Pro:** Massive industry demand; high compensation ceilings.<br>**Con:** Requires understanding code vulnerabilities, logic flaws, and automated scanning tools. |
| **3. Design → GRC, Privacy (DPDP) & Security Awareness** | Visual communication, empathy, workflow documentation, reading regulations, zero coding required. | Low to Medium | • Privacy Analyst<br>• Junior GRC Associate<br>• Security Awareness & Culture Specialist<br>• Compliance Analyst | **₹5 – 10 LPA** (Big 4, FinTech, Healthcare, GCCs) | High (Spurred by India DPDP Act 2023) | **Pro:** Lowest technical barrier; leverages presentation and visual communication; regular day shifts.<br>**Con:** Heavy document/framework reading (ISO 27001, NIST, SOC 2, DPDP). |
| **4. IT Support → SysAdmin / Endpoint → Security** | OS fundamentals (Windows/Linux), Active Directory, troubleshooting, customer handling. | Medium | • Service Desk Engineer<br>• Desktop Support Engineer<br>• Associate Endpoint Administrator | **₹3 – 5.5 LPA** (IT Services, MSPs) | Very High (Massive volume) | **Pro:** Most realistic non-degree entry point into formal IT; employer often sponsors certifications.<br>**Con:** Lower starting pay; requires 12–18 months before pivoting to internal security roles. |
| **5. NOC / Networking → Network Security / SOC** | TCP/IP, subnetting, switching, firewalls (Palo Alto, Fortinet), packet capture. | Medium to High | • Network Support Engineer<br>• Junior NOC Analyst<br>• Network Security Associate | **₹3.5 – 6.5 LPA** (Telecoms, MSPs, Data Centers) | High | **Pro:** Unshakeable networking foundation that makes you an elite defender or pentester.<br>**Con:** Involves rotating shifts; hardware-heavy troubleshooting. |
| **6. Cloud/IT Ops → Cloud Security** | Linux CLI, Cloud fundamentals (AWS/Azure), virtualization, IAM policies, Docker basics. | High | • Cloud Operations Associate<br>• Junior Cloud Security Engineer<br>• Infrastructure Analyst | **₹6 – 11 LPA** (GCCs, Cloud Consultancies) | High | **Pro:** Cloud is the dominant infrastructure for modern Indian tech; future-proof.<br>**Con:** Steep initial conceptual jump from pure design. |
| **7. Direct Entry-Level SOC (L1 Analyst)** | Networking, OS internals, SIEM concepts, log analysis, threat intelligence, triage workflows. | Medium to High | • SOC Analyst L1<br>• Incident Response Associate<br>• Cyber Defense Analyst | **₹3.5 – 6.5 LPA** (Services & MSSPs)<br>**₹7 – 12 LPA** (GCCs & Big 4) | Highest Volume | **Pro:** Direct security badge on day one; clear progression to L2/L3/Threat Hunting.<br>**Con:** 24/7 rotating night shifts; alert fatigue; high initial HR screening competition. |

---

## 3. The Indian Cybersecurity Job Market Reality

### Ecosystem Segmentation
1. **Global Capability Centers (GCCs) (Bengaluru, Hyderabad, Pune, Gurugram):**
   - Companies: Target, Walmart, Wells Fargo, Goldman Sachs, Standard Chartered, Lowe's India.
   - Profile: High compensation (₹8–15 LPA for early-career), focus on product security, GRC, internal SOC, and security UX. They evaluate practical skills and problem-solving over rigid degree labels.
2. **Indian IT Services & System Integrators (TCS, Infosys, Wipro, HCL, Cognizant, Tech Mahindra):**
   - Profile: Massive volume of L1 SOC and Managed Security Services (MSSP) contracts for global Fortune 500 clients.
   - Constraints: Strict automated resume filters (often insisting on 60%+ in 10th/12th/Graduation or B.Tech/BCA). If you have a non-tech degree, bypass standard portals via employee referrals or open-source proof of work.
3. **The Big 4 & Advisory Firms (Deloitte, PwC, EY, KPMG):**
   - Profile: Heavy demand for GRC, Cyber Strategy, Privacy Advisory (DPDP / GDPR), and Third-Party Risk Management (TPRM).
   - Advantage for Designers: High value placed on structured documentation, executive presentation skills, and business visual communication.
4. **Product Startups & Unicorns (CRED, Razorpay, Zerodha, Swiggy, Flipkart):**
   - Profile: Modern tech stacks (AWS, Kubernetes, Zero Trust), modern AppSec, DevSecOps, and UX friction balancing (e.g., seamless UPI transaction authentication UX).

### The DPDP Act 2023 Opportunity
The enactment of India's **Digital Personal Data Protection Act, 2023 (DPDP Act)** has created a distinct shortage of professionals who understand both **Data Privacy Compliance** and **User Experience Design**:
- Organizations require *Consent Managers*, *Clear Notice Designs* (in 22 official languages), *Cookie/Data flow transparencies*, and *User Rights Requests (Data Erasure/Access)* that are intuitive and legally compliant.
- Designers who learn GRC and privacy regulations can bridge this gap between legal teams, product managers, and developers.

### The Certification Reality in India
- **Do NOT fall for Indian ed-tech bootcamps** charging ₹1.5 to ₹3.5 Lakhs with misleading "100% placement guarantees." Most place candidates into standard non-security BPO/support roles.
- **HR Screening Filters:** In India, entry-level keyword scanners filter for:
  - *CompTIA Security+* (Universal baseline, respected in GCCs/MNCs).
  - *Microsoft SC-900 / AZ-900* (Very affordable at ~₹4,800 INR; widely respected in corporate IT environments).
  - *Certified AppSec Practitioner (CAP)* or *eJPT* (Hands-on proof for AppSec/Penetration Testing).
  - *ISO/IEC 27001 Lead Auditor/Implementer* (Gold standard for GRC roles).

---

## 4. Shared Foundations (Stage 0 to Stage 2)

Before selecting a specialized branch, every designer must complete this shared foundational path.

```
┌────────────────────────────────────────────────────────┐
│ Stage 0: OS Internals & Virtual Environments (Weeks 1-4)│
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Stage 1: Networking & Internet Architecture (Weeks 5-8)│
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Stage 2: Security Principles & Threat Models (Weeks 9-12)│
└────────────────────────────────────────────────────────┘
```

### Stage 0: Operating Systems & Virtualization Core
- **Concept:** How an operating system manages processes, memory, file systems, permissions, and network sockets.
- **Windows Internals:** NTFS permissions (Read, Write, Execute, Modify), Windows Registry, Services, Event Viewer (Security Event IDs 4624, 4625), Windows Defender Firewall.
- **Linux Fundamentals (Ubuntu / Fedora):** Root vs standard user, `sudo`, POSIX file permissions (`chmod`, `chown`), package management (`apt` / `dnf`), systemd services, SSH architecture.

### Stage 1: Networking & Internet Protocols
- **The OSI & TCP/IP Stack:** Physical layer to Application layer. Understand data encapsulation (Frame → Packet → Segment → Data).
- **Addressing:** IPv4 Private Ranges (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16), Subnetting, MAC addresses, Default Gateways, Loopback (127.0.0.1).
- **Core Protocols:**
  - **DNS (Port 53):** Resolving domain names to IP addresses. How attackers hijack or spoof DNS.
  - **DHCP (Ports 67/68):** Automatic IP assignment on local networks.
  - **HTTP/HTTPS (Ports 80/443):** Headers, Verbs (GET, POST, PUT, DELETE), Status Codes (200, 301, 401, 403, 404, 500), TLS/SSL handshakes, Public Key Infrastructure (PKI).
  - **SSH (Port 22), RDP (Port 3389), SMB (Port 445):** Remote administration and file sharing protocols.

### Stage 2: Core Security Principles
- **The CIA Triad:**
  - *Confidentiality:* Encryption at rest and in transit (AES, RSA, TLS).
  - *Integrity:* Cryptographic hashing (SHA-256), digital signatures.
  - *Availability:* Redundancy, backups, DDoS mitigation, uptime monitoring.
- **Authentication, Authorization & Accounting (AAA):**
  - Authentication = Who are you? (Passwords, Passkeys, TOTP 2FA, Biometrics).
  - Authorization = What are you allowed to do? (Role-Based Access Control - RBAC, Principle of Least Privilege).
  - Accounting = What did you do and when? (Audit logs, SIEM ingestion).
- **Threat Modeling Fundamentals:** STRIDE model (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege).

---

## 5. No-Router Home Lab Architecture (Windows 11)

### Why You Do Not Need Router Access
Many beginners mistakenly assume practicing network security and systems administration requires logging into their physical home Wi-Fi router (Airtel, Jio, ACT, etc.) to set up port forwarding or DMZs. **This is completely unnecessary and dangerous.**

Modern hypervisors (VMware Workstation Pro or Oracle VirtualBox) provide internal software-defined virtual switches:
1. **NAT Mode (Network Address Translation):** The hypervisor acts as a private router inside your Windows PC. VMs can access the public internet to download packages, but outside computers cannot see your VMs.
2. **Host-Only / Isolated Internal Network:** A dedicated virtual network switch created entirely inside your PC's RAM. VMs on this switch can only talk to each other and to the host PC. It is 100% air-gapped from your home physical router.

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

### Lab Setup: 5 Core Exercises (Pedagogical Command Breakdown)

#### Exercise 1: Isolating Your Virtual Network
- **Purpose:** Configure a dedicated virtual subnet for your lab VMs so no traffic touches your home LAN.
- **Tool:** VMware Workstation Pro (Virtual Network Editor) or VirtualBox (Tools → Network Manager).
- **Execution:** Create a Host-Only network named `HostOnlyNet` with subnet `192.168.56.0/24`. Set DHCP range from `192.168.56.10` to `192.168.56.50`.
- **Verification:** Run `ipconfig` on Windows host; verify an adapter named `VMware Network Adapter VMnet1` or `VirtualBox Host-Only Ethernet Adapter` has an IP in `192.168.56.x`.

---

#### Exercise 2: Linux User Privilege & File Permissions
In your Fedora/Ubuntu VM, create a restricted directory simulating confidential security documentation.

##### Step A: Create a dedicated group and user
- **Command:**
  ```bash
  sudo groupadd secops
  sudo useradd -m -g secops -s /bin/bash analyst1
  ```
- **Concept:** Linux organizes rights around users and groups. We create a group `secops` and assign the new user `analyst1` to it.
- **What it changes:** Appends entries to `/etc/group` and `/etc/passwd`; creates home directory `/home/analyst1`.
- **Risks:** Negligible on a local VM.
- **Expected Result:** Silent execution (zero output indicates success in Unix).
- **Verification:**
  ```bash
  id analyst1
  ```
  *(Output shows uid, gid, and membership in secops).*
- **Undo:**
  ```bash
  sudo userdel -r analyst1
  sudo groupdel secops
  ```

##### Step B: Create a secure directory and enforce POSIX permissions
- **Command:**
  ```bash
  sudo mkdir /opt/secure_reports
  sudo chown root:secops /opt/secure_reports
  sudo chmod 770 /opt/secure_reports
  ```
- **Concept:**
  - `chown root:secops` sets the owning user to `root` and owning group to `secops`.
  - `chmod 770`:
    - `7` (rwx) for Owner (`root`)
    - `7` (rwx) for Group (`secops`)
    - `0` (---) for Others (all other users have zero read, write, or execute rights).
- **What it changes:** Updates the inode metadata for `/opt/secure_reports`.
- **Risks:** None in this test path.
- **Expected Result:** Any user outside `secops` is blocked with `Permission denied`.
- **Verification:**
  ```bash
  ls -ld /opt/secure_reports
  # Expected: drwxrwx--- 2 root secops ... /opt/secure_reports
  ```
- **Undo:**
  ```bash
  sudo rm -rf /opt/secure_reports
  ```

---

#### Exercise 3: Hardening SSH Authentication
Replace password-based login with cryptographic public/private key pairs.

##### Step A: Generate an SSH Keypair on Windows Host (PowerShell)
- **Command:**
  ```powershell
  ssh-keygen -t ed25519 -C "designer-lab-key" -f $HOME\.ssh\id_lab_ed25519
  ```
- **Concept:** Ed25519 is a state-of-the-art elliptic-curve digital signature algorithm. It creates two files:
  - Private key: `id_lab_ed25519` (Must NEVER leave your host PC).
  - Public key: `id_lab_ed25519.pub` (Can be safely shared with any server you want to access).
- **What it changes:** Writes two key files into `C:\Users\<YourUser>\.ssh\`.
- **Risks:** If you overwrite an existing key with the same name, previous server connections using it will break.
- **Expected Result:** Fingerprint and randomart image displayed in PowerShell.
- **Verification:**
  ```powershell
  Get-ChildItem $HOME\.ssh\id_lab_ed25519*
  ```

##### Step B: Authorize the key on your Linux VM
- **Concept:** The Linux SSH daemon reads `~/.ssh/authorized_keys` to authenticate incoming login requests.
- **Command (Inside Linux VM):**
  ```bash
  mkdir -p ~/.ssh
  chmod 700 ~/.ssh
  nano ~/.ssh/authorized_keys
  # Paste the text from id_lab_ed25519.pub here, save and exit
  chmod 600 ~/.ssh/authorized_keys
  ```
- **Security Check:** `chmod 700` and `600` ensure no other user on the VM can read your authorized keys or inject their own.

##### Step C: Test Key Connection from Windows Host
- **Command:**
  ```powershell
  ssh -i $HOME\.ssh\id_lab_ed25519 username@192.168.56.X
  ```
- **Expected Result:** Instant shell access without prompting for the user's password.

---

#### Exercise 4: Host-Based Firewall Rules (UFW / Firewalld)
- **Concept:** A host-based firewall filters network packets entering and leaving the individual machine operating system, even if the surrounding local network is untrusted.
- **Command (Ubuntu `ufw`):**
  ```bash
  # Check status
  sudo ufw status verbose
  # Set default policy: block all incoming, allow all outgoing
  sudo ufw default deny incoming
  sudo ufw default allow outgoing
  # Allow only SSH from the private host-only subnet
  sudo ufw allow from 192.168.56.0/24 to any port 22 proto tcp
  # Enable firewall
  sudo ufw enable
  ```
- **What it changes:** Modifies Linux kernel Netfilter tables (`iptables`/`nftables`).
- **Risks:** If you enable the firewall without allowing port 22, remote SSH disconnects. Always ensure VM console access is available in the hypervisor window.
- **Expected Result:** `Firewall is active and enabled on system startup`.
- **Verification:**
  ```bash
  sudo ufw status numbered
  ```
- **Undo:**
  ```bash
  sudo ufw disable
  sudo ufw reset
  ```

---

#### Exercise 5: Safe Backup & Restore Simulation
- **Concept:** Availability is 1/3rd of the CIA triad. Backups must be tested for integrity and restoration, not just creation.
- **Command (Archiving configuration files):**
  ```bash
  sudo tar -czvf /tmp/etc_ssh_backup_$(date +%F).tar.gz /etc/ssh
  ```
- **Concept:** `tar` packages multiple files into an archive; `-z` compresses it with gzip; `$(date +%F)` timestamps the archive.
- **Verification (Integrity Test):**
  ```bash
  tar -ztvf /tmp/etc_ssh_backup_*.tar.gz
  ```
  *(Lists all archived files without extracting, confirming the archive is not corrupt).*
- **Undo / Cleanup:**
  ```bash
  rm /tmp/etc_ssh_backup_*.tar.gz
  ```

---

## 6. Specialized Career Branches

```
                    ┌─────────────────────────┐
                    │   Shared Foundations    │
                    │   (Stages 0, 1, and 2)  │
                    └────────────┬────────────┘
         ┌──────────────────────┼──────────────────────┐
         │                      │                      │
┌────────▼────────┐    ┌────────▼────────┐    ┌────────▼────────┐
│  Branch 1:      │    │  Branch 2:      │    │  Branch 3:      │
│  Security UX &  │    │  AppSec &       │    │  GRC, Privacy & │
│  Product Design │    │  Web Security   │    │  Security Aware │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                      │                      │
┌────────▼────────┐    ┌────────▼────────┐    ┌────────▼────────┐
│  Branch 4:      │    │  Branch 5:      │    │  Branch 6:      │
│  SOC & Blue     │    │  Identity &     │    │  Cloud Security │
│  Team Defense   │    │  Access (IAM)   │    │  (AWS / Azure)  │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

---

### Branch 1: Security UX, Human Factors & Secure Product Design

#### Core Competency Focus
- Designing intuitive security warnings that users actually read (combating "warning fatigue").
- Authentication UX: Passkeys, WebAuthn, biometric onboarding, 2FA recovery flows.
- Friction balancing: Applying intentional friction (interstitial confirmation screens, friction gates) during irreversible or high-risk actions (e.g., banking fund transfers, API key deletion).
- Privacy-by-Design: Clear consent architectures, granular permission requests, transparent data-sharing dashboards.

#### Free Learning Path
- **NIST Special Publication 800-63:** Digital Identity Guidelines (Enrollment, Authentication, Federation).
- **Carnegie Mellon CyLab Usable Privacy and Security Laboratory:** Open-access research papers on human factors in cyber.
- **FIDO Alliance Documentation:** Specifications on Passkeys and UX guidelines for passwordless authentication.
- **Google Material Design Security & Privacy Patterns:** Guidelines for permissions, location access, and authentication prompts.

#### Capstone Portfolio Project
- **Project: "Enterprise IAM & MFA Fallback Experience Redesign"**
  - *Objective:* Redesign the multi-factor authentication (MFA) and account recovery workflow for an enterprise SaaS platform.
  - *Artifact:* Interactive Figma prototype + Case Study detailing:
    1. Usability test results analyzing where users get locked out.
    2. Prevention of "MFA Fatigue Attacks" (Prompt bombing) by replacing single-tap approval with number-matching verification.
    3. Emergency fallback protocol balancing security against helpdesk workload.

---

### Branch 2: Web & Application Security (AppSec)

#### Core Competency Focus
- Deep understanding of the **OWASP Top 10** (Injection, Broken Authentication, Sensitive Data Exposure, Broken Access Control, Security Misconfiguration, XSS, SSRF).
- Client-server architecture: Inspecting HTTP requests with proxy tools (Burp Suite Community Edition).
- Understanding how modern front-end design choices (React, Vue, DOM rendering) impact client-side security (DOM XSS, CORS misconfigurations, CSRF).

#### Free Learning Path
- **PortSwigger Web Security Academy (100% Free):** The single best web security training platform globally. Complete the Apprentice and Practitioner tracks for SQLi, XSS, CSRF, and Access Control.
- **OWASP Juice Shop:** A deliberately vulnerable modern web application (Node.js/Angular). Run it locally in Docker or Hypervisor.
- **OWASP Application Security Verification Standard (ASVS):** The industry standard checklist for designing secure web apps.

#### Capstone Portfolio Project
- **Project: "Vulnerability Remediation & Threat Model of a Designer Portfolio CMS"**
  - *Objective:* Deploy OWASP Juice Shop or a simple web app locally, map vulnerabilities with Burp Suite Community, and write a professional remediation report.
  - *Artifact:* A GitHub repository containing:
    1. Threat model diagram using STRIDE.
    2. Vulnerability report formatted with CVSS scoring, steps to reproduce, HTTP request/response proofs, and code-level remediation advice for the developers.

---

### Branch 3: GRC, Privacy (DPDP Act 2023) & Security Awareness

#### Core Competency Focus
- **Regulatory Frameworks:** ISO/IEC 27001:2022 (Information Security Management System), NIST Cybersecurity Framework (CSF 2.0: Govern, Identify, Protect, Detect, Respond, Recover), SOC 2 Type II compliance.
- **Data Protection Regulations:** India's DPDP Act 2023, EU GDPR, ISO 27701 (Privacy Information Management).
- **Security Awareness & Culture:** Designing human risk training, anti-phishing communication campaigns, executive security dashboards, and compliance documentation.

#### Free Learning Path
- **Ministry of Electronics and Information Technology (MeitY):** Official Gazette copy and explanatory releases of the Digital Personal Data Protection Act, 2023.
- **NIST CSF 2.0 Official Learning Material:** Free guides and implementation tiers provided by NIST.gov.
- **SANS Security Awareness Worksheets:** Free community resources for building organizational security culture.
- **ISO 27001 Introduction Summaries:** High-level clauses (Context, Leadership, Risk Assessment, Annex A controls).

#### Capstone Portfolio Project
- **Project: "DPDP Act 2023 Compliance & Consent Architecture Toolkit"**
  - *Objective:* Build an end-to-end compliance toolkit for an Indian consumer-facing application (e-commerce or healthcare).
  - *Artifact:* Public GitHub repository / Notion portfolio containing:
    1. Data Flow Map tracking Personal Data collection to storage.
    2. User-facing Consent Notice wireframes compliant with Section 5 of the DPDP Act.
    3. Phishing simulation campaign communication pack (infographics, alert templates, training slide decks).

---

### Branch 4: Security Operations Center (SOC) & Blue Team

#### Core Competency Focus
- Log analysis: Windows Event Logs, Sysmon, Linux Syslog, Web Server logs (NGINX/Apache).
- Security Information and Event Management (SIEM): Querying, filtering, and alert correlation using Splunk or Elastic Security.
- Incident Response: Identification, Containment, Eradication, and Post-Incident Reporting (NIST SP 800-61r2).
- Threat Intelligence: MITRE ATT&CK framework mapping.

#### Free Learning Path
- **TryHackMe (Free Rooms):** Pre-Security Path, Cyber Defense Introduction, "Intro to SIEM", "Splunk Basics".
- **Cisco Skills for All (100% Free):** "Introduction to Cybersecurity" and "Cybersecurity Threat Management".
- **Microsoft Learn:** Free self-paced learning paths for SC-200 (Microsoft Security Operations Analyst).
- **Boss of the SOC (BOTS) Datasets:** Free Splunk datasets to practice hunting realistic incident scenarios.

#### Capstone Portfolio Project
- **Project: "Local Wazuh SIEM Home Lab & Brute-Force Detection Pipeline"**
  - *Objective:* Deploy Wazuh Manager (open-source SIEM/XDR) on your local Linux VM; install Wazuh Agent on Windows.
  - *Artifact:* A published technical blog/writeup detailing:
    1. Architecture diagram of log forwarding over the private host-only network.
    2. Simulation of SSH brute-force attacks and RDP failed logins.
    3. Wazuh dashboard visualization and automated active-response containment rule.

---

### Branch 5: Identity & Access Management (IAM)

#### Core Competency Focus
- Directory Services: Microsoft Active Directory (AD), Azure AD (Microsoft Entra ID), LDAP.
- Modern Identity Protocols: OAuth 2.0, OpenID Connect (OIDC), SAML 2.0, SCIM (System for Cross-domain Identity Management).
- Zero Trust Architecture: Continuous verification, device health compliance, conditional access policies.

#### Free Learning Path
- **Microsoft Learn - Microsoft Entra ID Fundamentals:** Free documentation and sandbox walkthroughs.
- **Auth0 by Okta Identity Architecture Guides:** Free comprehensive guides on OAuth 2.0 grant types and JWT tokens.
- **Ping Identity / Okta Developer Portals:** Free developer tenants for hands-on SSO and MFA configuration.

#### Capstone Portfolio Project
- **Project: "Zero Trust Conditional Access Policy Architecture for a Hybrid Organization"**
  - *Objective:* Design a complete RBAC and Conditional Access matrix for a 250-person enterprise.
  - *Artifact:* Specification document containing:
    1. Role hierarchy (Admin, HR, Engineering, Contract Designer).
    2. Step-up authentication triggers (unrecognized location, risky sign-in).
    3. Lifecycle management workflow (Joiner, Mover, Leaver automation rules).

---

### Branch 6: Cloud Security

#### Core Competency Focus
- Cloud Architecture: Shared Responsibility Model (IaaS, PaaS, SaaS).
- Identity & Permissions in the Cloud: AWS IAM policies (JSON), Azure Role Assignments, Least Privilege enforcement.
- Infrastructure as Code (IaC) & Misconfiguration Auditing: Identifying open S3 buckets, exposed security groups, unencrypted databases.

#### Free Learning Path
- **AWS Skill Builder (Free Tier):** AWS Cloud Practitioner Essentials.
- **Microsoft Learn:** AZ-900 (Azure Fundamentals) and AZ-500 (Azure Security Technologies) free modules.
- **Flaws.cloud & Flaws2.cloud:** Free hands-on challenges teaching common AWS security mistakes.

#### Capstone Portfolio Project
- **Project: "AWS Secure Baseline Architecture Design & Terraform Audit"**
  - *Objective:* Build and audit a secure single-region cloud infrastructure baseline.
  - *Artifact:* GitHub repo containing:
    1. Network topology diagram (VPC, public/private subnets, NAT Gateway, Security Groups).
    2. Policy document restricting root account usage and enforcing MFA.
    3. Scans of Terraform files using free tools (Checkov / tfsec) with remediation notes.

---

## 7. Free vs. Paid Resource Breakdown

### 100% Free Core Resources (Start Here)
- **Networking & Foundations:** Professor Messer's Network+ & Security+ Training Courses (Free on YouTube).
- **Linux Mastery:** Linux Journey (`linuxjourney.com`), OverTheWire Bandit (`overthewire.org/wargames/bandit`).
- **Web Application Security:** PortSwigger Web Security Academy (`portswigger.net/web-security`).
- **Defense & SOC Skills:** Cisco Skills for All, Splunk Free Training (Splunk Fundamentals), Microsoft Learn modules.
- **Policy & Frameworks:** NIST SP publications, MeitY DPDP Act resources, OWASP Cheat Sheet Series.

### High-Value Paid Certifications (Only When Financially Ready)
*Never purchase until you have finished the free foundational syllabus and hands-on labs.*

| Certification | Provider | Estimated Cost (INR) | Value in Indian Job Market | Target Domain |
| :--- | :--- | :--- | :--- | :--- |
| **Microsoft SC-900** | Microsoft | ~₹4,800 (Often discounted via Student/Events) | High HR screening value for entry-level cloud & security foundations. | Foundations / Cloud / GRC |
| **CompTIA Security+ (SY0-701)** | CompTIA | ~₹32,000 – ₹35,000 | Globally recognized standard; required by many MNCs and US defense contractors in India. | SOC / General Security |
| **ISO/IEC 27001:2022 Lead Auditor** | BSI / TÜV / CQI-IRCA | ~₹22,000 – ₹35,000 | The single most respected credential for GRC and compliance advisory in Big 4 and IT services. | GRC / Compliance |
| **Certified AppSec Practitioner (CAP)** | The SecOps Group | ~₹8,000 – ₹12,000 | Practical, entry-level, affordable validation of web application security skills. | AppSec |
| **eJPT (eLearnSecurity Junior Penetration Tester)** | INE Security | ~₹22,000 ($249 USD) | 100% hands-on dynamic lab exam; proves real technical capability over multiple-choice tests. | VAPT / Offensive |

---

## 8. Roadmap.sh "Text to Roadmap" Formatted Code

Copy and paste the raw block below into the **"Text to Roadmap"** generator at [roadmap.sh](https://roadmap.sh):

```text
# Designer to Cybersecurity Transition Roadmap
## Phase 1: Shared Core Foundations
### Operating System Internals
- Windows Architecture & Event Logs
- Linux CLI & User Administration
- POSIX File Permissions & Access Control
- Virtualization & Hypervisor Networking

### Networking & Internet Architecture
- OSI 7-Layer & TCP/IP Model
- IPv4 Subnetting & Private Addresses
- DNS, DHCP, ARP & Packet Routing
- HTTP, HTTPS, TLS & Status Codes
- Common Ports: 22, 53, 80, 443, 3389

### Core Security & Threat Principles
- CIA Triad: Confidentiality, Integrity, Availability
- Authentication vs Authorization (AAA)
- Principle of Least Privilege
- Threat Modeling with STRIDE
- Defense in Depth Architecture

## Phase 2: Safe Local Home Lab
### Hypervisor & Network Isolation
- VMware Workstation Pro / VirtualBox Setup
- Host-Only & Internal Software Virtual Switches
- Zero Physical Router Access Constraint
- Static IP Assignment on Private Subnets

### Core Hands-on Lab Drills
- Linux Hardening & Sudoers Configuration
- SSH Keypair Generation & Password Login Disablement
- Host Firewall Configuration with UFW / Firewalld
- Automated Backup & Tarball Integrity Verification
- Log Inspection via Systemd Journal & Event Viewer

## Phase 3: Specialization Branches
### Security UX & Human Factors
- Usable Security & Warning Design
- Passkeys, FIDO2 & WebAuthn Flows
- Reducing Authentication Friction & MFA Fatigue
- Privacy by Design & Consent Architecture
- User Research on Security Mental Models

### Web & Application Security
- OWASP Top 10 Web Vulnerabilities
- PortSwigger Web Security Academy Labs
- Burp Suite Interception & HTTP Analysis
- Cross-Site Scripting (XSS) & SQL Injection
- Broken Access Control & Logic Flaws
- Secure Code Review & Remediation Reports

### GRC, Privacy & Security Awareness
- India DPDP Act 2023 Implementation
- ISO/IEC 27001:2022 Framework & Annex A
- NIST Cybersecurity Framework (CSF 2.0)
- SOC 2 Type II Trust Services Criteria
- Security Awareness Campaign & Phishing Training

### SOC Analyst & Blue Team
- Windows Security Event Log Correlation
- SIEM Fundamentals: Splunk & Elastic
- Wazuh Open Source SIEM & Agent Deployment
- Incident Handling Process (NIST SP 800-61)
- MITRE ATT&CK TTP Mapping

### Identity & Access Management (IAM)
- Active Directory & Microsoft Entra ID
- Single Sign-On (SSO) with SAML & OIDC
- OAuth 2.0 Authorization Workflows
- Role-Based Access Control (RBAC) Design
- Zero Trust Conditional Access Policies

### Cloud Security
- Shared Responsibility Model
- AWS & Azure Core Architecture
- Cloud IAM Policies & Least Privilege
- S3 Bucket & Security Group Auditing
- Infrastructure as Code (IaC) Security Scans

## Phase 4: Portfolio & Indian Market Launch
### Proof of Work Portfolio
- GitHub Technical Lab Documentation
- Figma Security UX Case Studies
- Threat Model & Vulnerability Writeups
- DPDP Act Compliance Templates

### Resume & Job Search Strategy
- Translation of Design Skills to Cyber Value
- LinkedIn Networking with Indian Infosec Community
- Targeting GCCs, Big 4, Services & Startups
- Navigating Indian HR Degree Filters
```

---

## 9. Portfolio, Resume & Indian Interview Preparation

### Reframing Design Experience for Cybersecurity
Designers possess distinct cognitive strengths that pure computer science graduates often lack:
1. **User Mental Models:** You understand how humans make mistakes. In cybersecurity, human error accounts for over 70% of breaches. You can frame this as expertise in **Human Risk Management** and **Social Engineering Defense**.
2. **Systems Thinking & Flowcharts:** User journey maps, wireframes, and design systems translate directly into **Threat Modeling Data Flow Diagrams (DFDs)** and **Incident Response Runbooks**.
3. **Cross-Functional Communication:** Designers constantly articulate technical constraints to non-technical stakeholders—the exact skill required for **GRC Advisory**, **Security Awareness**, and **CISO Executive Reporting**.

### Portfolio Structure (Host on GitHub Pages / Notion / Substack)
Do not present an empty resume. Build a 3-part public portfolio:
1. **The Architecture Lab Report:** Document your no-router home lab with clear diagrams, network layouts, and command explanations (demonstrating technical literacy).
2. **The Specialization Capstone:**
   - If *Security UX:* A full Figma case study redesigning an authentication/privacy workflow.
   - If *AppSec:* PortSwigger lab completion badges + a remediation writeup of a local vulnerable app.
   - If *GRC:* A complete DPDP Act 2023 readiness assessment checklist and visual consent flow for an Indian startup.
   - If *SOC:* Step-by-step Wazuh log analysis report detecting simulated attacks.
3. **Technical Blog Posts:** Write 2–3 LinkedIn or Medium articles deconstructing a recent Indian security incident (e.g., an Aadhaar data leak, a UPI phishing scam) from your combined design and security perspective.

### Top Indian Interview Questions to Master
1. **Foundations:** *"Explain what happens under the hood when a user types `https://bank.com` into their browser and presses Enter."* (Explain DNS query, TCP three-way handshake, TLS handshake, HTTP GET request, server response).
2. **Design to Security Transition:** *"Why are you switching from design to security? Isn't design completely unrelated?"* (Emphasize human-centric security, friction balancing, threat modeling, and how security products fail when they ignore usability).
3. **Defensive Thinking:** *"What is the difference between Authentication and Authorization? Give a real-world web application example."*
4. **Scenario Handling:** *"An employee in an Indian IT office receives a suspicious email appearing to come from HR with an updated Diwali bonus PDF. What technical and human controls prevent compromise?"*

---

## Repository Maintenance
This repository is managed on branch `arena/1c08423d-design-to-cyber`. All roadmap updates, lab exercise guides, and study materials are tracked version-by-version.
