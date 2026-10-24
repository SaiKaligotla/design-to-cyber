# The Designer to Cybersecurity Master Roadmap & Interview Playbook

[![Audience](https://img.shields.io/badge/Audience-Designers%20%26%20Non--Tech%20Switchers-brightgreen.svg)](#)
[![Focus](https://img.shields.io/badge/Focus-Conquering%20the%20Interview%20Stage-orange.svg)](#)
[![Market](https://img.shields.io/badge/Market-India%20(SOC%20%7C%20IAM%20%7C%20SecOps)-blue.svg)](#)
[![Budget](https://img.shields.io/badge/Budget-%E2%82%B90%20(100%25%20Free--First)-purple.svg)](#)

A structured, battle-tested career transition roadmap designed specifically for **designers (UI/UX, visual, product, graphic) and non-technical career switchers** to systematically learn cybersecurity, build an unassailable hands-on proof-of-work portfolio, and **conquer the technical scenario-based interview stage** in India.

---

## Table of Contents
1. [The Real Reason Non-Tech Switchers Fail at the Interview Stage](#1-the-real-reason-non-tech-switchers-fail-at-the-interview-stage)
2. [Translating Design Thinking into Cybersecurity Superpowers](#2-translating-design-thinking-into-cybersecurity-superpowers)
3. [The Complete 5-Stage Detection & Triage Lab (Windows 11 | Zero Router Access)](#3-the-complete-5-stage-detection--triage-lab-windows-11--zero-router-access)
4. [Mastering the Technical Scenarios That Screen Candidates Out](#4-mastering-the-technical-scenarios-that-screen-candidates-out)
   - [Scenario A: Brute Force & Post-Compromise Detection](#scenario-a-brute-force--post-compromise-detection)
   - [Scenario B: RFC 822 Email Header Forensics & Phishing Triage](#scenario-b-rfc-822-email-header-forensics--phishing-triage)
   - [Scenario C: The Service Account Trap (Avoiding Self-Inflicted Outages)](#scenario-c-the-service-account-trap-avoiding-self-inflicted-outages)
   - [Scenario D: Ransomware & EDR Host Isolation (Preserving Memory Artifacts)](#scenario-d-ransomware--edr-host-isolation-preserving-memory-artifacts)
5. [Windows Event Log Mastery: Beyond Event ID 4625](#5-windows-event-log-mastery-beyond-event-id-4625)
6. [The 60-Day Step-by-Step Transition & Interview-Readiness Plan](#6-the-60-day-step-by-step-transition--interview-readiness-plan)
7. [How to Answer: "Why Are You Switching from Design?"](#7-how-to-answer-why-are-you-switching-from-design)
8. [Repository Structure & Detailed Playbooks](#8-repository-structure--detailed-playbooks)

---

## 1. The Real Reason Non-Tech Switchers Fail at the Interview Stage

Most designers and non-STEM candidates who transition into cybersecurity successfully clear online multiple-choice courses (such as the Google Cybersecurity Certificate or introductory security modules), but **consistently fail at the technical interview round**.

### The 4 Lethal Gaps in Technical Interviews

```
┌────────────────────────────────────────────────────────┐
│ Gap 1: Reciting Book Definitions vs. Operational Flow   │
│ Candidates explain WHAT a concept is, not HOW to triage│
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Gap 2: The "Surface Log" Illusion                      │
│ Memorizing Event ID 4625 without knowing Logon Types   │
│ (Type 2 vs 3 vs 10) or Sub-status codes (0xC000006A)   │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Gap 3: The Blast Radius & Production Awareness Trap    │
│ Recommending destructive containment (locking service  │
│ accounts or rebooting machines during active attacks)  │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Gap 4: Passive Homelabs (No Attack-to-Detection Cycle) │
│ Merely "viewing" logs instead of generating attacks,   │
│ tuning SIEM rules, and producing formal incident briefs│
└────────────────────────────────────────────────────────┘
```

When an Indian interviewer at an MSSP, Global Capability Center (GCC), or tech company asks a scenario question, they are **not** testing memory. They are evaluating:
> *"Can this person sit in front of an active SIEM/EDR queue at 2 AM, investigate an alert without panicking, distinguish a true attack from a benign glitch, and take containment steps without crashing our production business services?"*

---

## 2. Translating Design Thinking into Cybersecurity Superpowers

You do not need an engineering degree to be an elite security analyst. In fact, mature cybersecurity operations value the exact cognitive models that designers use daily:

| Design Competency | Equivalent Cybersecurity Superpower | Why Interviewers Value This |
| :--- | :--- | :--- |
| **User Journey Mapping & Flows** | **Attack Path & Data Flow Analysis (STRIDE / MITRE ATT&CK)** | Pentesters and threat analysts map how an adversary moves step-by-step from initial phishing click to database exfiltration. |
| **Edge Cases & Error State Design** | **Abuse Case Analysis & Exploit Modeling** | Designers constantly ask: *"What if the user clicks back twice or enters invalid input?"* Security analysts ask the exact same question to identify business logic flaws and authentication bypasses. |
| **Cognitive Load & Usability Friction** | **Social Engineering Defense & Human Risk Analysis** | Over 74% of enterprise breaches involve human error (phishing, MFA fatigue). Designers understand human mental models, habituation, and deceptive dark patterns better than pure programmers. |
| **Design Systems & Component Standards** | **Hardening Baselines & Configuration Auditing (CIS Benchmarks)** | Maintaining a consistent Figma component library requires the exact same structural discipline as enforcing Active Directory Group Policy (GPO) and baseline endpoint hardening. |

---

## 3. The Complete 5-Stage Detection & Triage Lab (Windows 11 | Zero Router Access)

### Why Just "Viewing Windows Logs" Fails in Interviews
Simply opening `eventvwr.msc` and looking at event IDs is passive and unimpressive. A credible homelab must demonstrate an **end-to-end detection, correlation, and response cycle**:

```
[ Attacker: Kali Linux VM ] ──(Hydra / Atomic Red Team)──► [ Target: Windows 11 / Server VM ]
                                                                      │
                                                           Sysmon Enhanced Telemetry
                                                           (Process Create, Network Conn)
                                                                      │
                                                                Winlogbeat / Wazuh Agent
                                                                      │
                                                                      ▼
                                                           [ Detection Engine: Wazuh / Splunk ]
                                                                      │
                                                           Alert Correlation & Rule Tuning
                                                                      │
                                                                      ▼
                                                           [ SOC Triage & Containment Report ]
```

### Lab Setup (Isolated Host-Only Virtual Switch — Zero Router Access Needed)
Modern hypervisors (VMware Workstation Pro or Oracle VirtualBox) provide a **Host-Only virtual switch** created entirely inside your PC's memory. The VMs communicate securely with each other and your host, completely isolated from your home Wi-Fi router.

#### Stage 1: Installing Enhanced Telemetry (Sysmon)
Default Windows logs do not capture process command-line arguments or parent processes.
1. Download Microsoft Sysinternals **Sysmon** on your target Windows VM.
2. Download the industry-standard **SwiftOnSecurity Sysmon configuration XML**.
3. Install via Administrator command prompt:
   ```cmd
   sysmon.exe -accepteula -i sysmonconfig-export.xml
   ```
4. **What this enables:**
   * **Event ID 1:** Process Creation (captures the full command line, parent process name, SHA-256 hash).
   * **Event ID 3:** Network Connection (captures destination IP, port, and the exact executable that initiated it).
   * **Event ID 11:** File Creation (captures dropped payloads and ransomware staging).

#### Stage 2: Attack Simulation (From Kali VM)
Simulate realistic adversary behaviors:
* **Attack Drill 1 (SSH / RDP Brute Force):**
  ```bash
  hydra -l administrator -P /usr/share/wordlists/rockyou.txt ssh://<Linux_Target_IP>
  ```
* **Attack Drill 2 (Living off the Land / LOLBAS Payload Execution):**
  Simulate an attacker using encoded PowerShell on the Windows target:
  ```powershell
  powershell.exe -ExecutionPolicy Bypass -WindowStyle Hidden -Command "Write-Output 'Simulated Threat Activity'"
  ```

#### Stage 3: Ingestion & Custom Rule Tuning (Wazuh / Splunk)
1. **Wazuh Manager:** Inspect `/var/ossec/logs/alerts/alerts.json`.
2. **Rule Tuning:** Edit `/var/ossec/etc/rules/local_rules.xml` to create an aggregated rule: alert Level 10 when 5 failed logons occur within 60 seconds from the same IP address.
3. **Splunk Search Processing Language (SPL):** In your free local Splunk instance, search:
   ```spl
   index=windows (EventCode=4625 OR EventCode=1)
   | stats count by user, src_ip, Image, CommandLine
   | where count > 3
   ```

#### Stage 4: Triage & Indicator Enrichment
* Extract the external IP, domain, and hash.
* Enrich via free tools: **VirusTotal**, **URLScan.io**, and **AbuseIPDB**.
* Confirm whether the event is a **True Positive** (authorized red team drill) or **False Positive**.

#### Stage 5: Containment & Incident Documentation
* Execute containment: block the IP via local firewall (`sudo ufw deny from <Attacker_IP>`) or isolate the VM.
* Write a professional incident report following **NIST SP 800-61** with **MITRE ATT&CK mapping (T1110.001 - Password Guessing)**. Publish this report to your public GitHub portfolio.

---

## 4. Mastering the Technical Scenarios That Screen Candidates Out

### Scenario A: Brute Force & Post-Compromise Detection
* **The Interview Question:** *"You see an alert for 50 failed logons within 3 minutes on user 'Rahul', followed by a successful logon. What do you do?"*
* **The Winning Response:**
  1. **Treat as Likely Compromise:** Treat the successful login as an active compromise resulting from credential guessing.
  2. **Inspect Sub-fields:** Check Event ID 4625 for **Logon Type** (Type 10 = RDP, Type 3 = SMB/Network) and Sub-status code (`0xC000006A` = wrong password for existing account).
  3. **Audit Post-Auth Activity:** The primary task is determining what happened **after** the successful Event ID 4624. Check Sysmon Event ID 1 for suspicious child processes (`whoami`, `net user`, `cmd.exe`) and anomalous outbound network connections (Sysmon Event ID 3).
  4. **Containment:** Revoke all active sessions in Azure AD / Entra ID, force a password reset, temporarily disable the account, and block the external source IP on the firewall.
  5. **Persistence Check:** Check for newly created scheduled tasks (Event ID 4698) or new local users (Event ID 4720).

---

### Scenario B: RFC 822 Email Header Forensics & Phishing Triage
* **The Interview Question:** *"An employee forwards a suspicious email claiming their salary slip is attached. How do you analyze it?"*
* **The Winning Response:**
  1. **Never Click:** Open the email in an isolated sandbox and extract the raw RFC 822 headers.
  2. **Sender Alignment:** Compare the header `From:` address (display name) with the envelope sender (`Return-Path:`). Phishing attacks frequently spoof the display name while the `Return-Path` points to an attacker-controlled domain.
  3. **Inspect Authentication Flags:**
     * **SPF (Sender Policy Framework):** Verifies if the sending server IP is authorized by the domain's DNS TXT record.
     * **DKIM (DomainKeys Identified Mail):** Verifies the email body and headers were cryptographically signed and not tampered with in transit.
     * **DMARC (Domain-based Message Authentication):** Verifies alignment between SPF/DKIM and the `From:` header (`p=reject`, `p=quarantine`, or `p=none`).
  4. **Inspect Received Hops:** Trace the `Received:` headers chronologically from bottom to top to identify the originating server IP and Mail Transfer Agent (MTA).
  5. **Defanged Enrichment:** Defang URLs (`hxxps[://]...`) and check them on URLScan.io and VirusTotal. If an attachment exists, calculate its SHA-256 hash in terminal (`sha256sum attachment.pdf`) and search malware databases.
  6. **Enterprise Scope:** Query the mail gateway (Microsoft Defender for Office 365 / Mimecast) using the `Message-ID` to purge the email from all employee inboxes.

---

### Scenario C: The Service Account Trap (Avoiding Self-Inflicted Outages)
* **The Interview Question:** *"An alert triggers for 500 failed logons in 5 minutes on `svc_sap_sync`. Do you immediately disable the account?"*
* **The Winning Response:**
  > *"No. Immediately locking a critical service account can crash enterprise production operations (e.g. database replication or ERP systems), causing a self-inflicted Denial of Service.
  > 
  > In corporate environments, over 80% of service account failure surges are caused by **internal IT password rotations**: an admin changed the service account password in Active Directory, but forgot to update a background script or scheduled task on one server, which continuously retries with stale credentials.
  > 
  > I check the source IP. If it is an internal application server, I identify the process and alert the application owner. If the source IP is untrusted or external, I contain the **source host** via firewall rules or host isolation, neutralizing the attack while keeping the production service operational."*

---

### Scenario D: Ransomware & EDR Host Isolation (Preserving Memory Artifacts)
* **The Interview Question:** *"An alert flags an endpoint running `vssadmin delete shadows /all /quiet`. What is your immediate action?"*
* **The Winning Response:**
  1. **Recognize Pre-Ransomware Indicator:** Adversaries delete Volume Shadow Copies to prevent system recovery before deploying ransomware encryption.
  2. **EDR Host Isolation (DO NOT REBOOT):** Immediately isolate the endpoint from the network using EDR. **Never power down or reboot the computer.** Powering down destroys volatile memory (RAM), which contains unencrypted encryption keys, running malware process injections, and live network connections necessary for forensic analysis.
  3. **Trace Process Lineage:** Inspect the parent process in Sysmon/EDR: Did `powershell.exe` or `cmd.exe` spawn from an Office document or an unknown binary?
  4. **Fleet Scoping:** Search the SIEM/EDR across all enterprise endpoints for that executable hash to identify lateral movement.

---

## 5. Windows Event Log Mastery: Beyond Event ID 4625

To pass Indian SOC/SecOps interviews, you must know the exact **Logon Types** and **Sub-Status Failure Codes**:

### Core Windows Logon Types
* **Type 2 (Interactive):** Physical keyboard/console login on the local machine.
* **Type 3 (Network):** Connection over the network (accessing an SMB file share, `PsExec`, or mapping a drive). Central to lateral movement investigations.
* **Type 4 (Batch):** Scheduled task executing under a specific service account.
* **Type 5 (Service):** Windows Service started by the Service Control Manager.
* **Type 10 (RemoteInteractive / RDP):** Remote Desktop Protocol connection. Crucial for detecting external brute-force attacks against internet-facing endpoints.

### Core Failure Sub-Status Codes (Inside Event 4625)
* **`0xC000006A` (Bad Password):** The username exists in the domain/workgroup, but the password was incorrect. (Indicates brute force or password spraying).
* **`0xC0000064` (User Name does not exist):** The username entered does not exist. (Indicates user enumeration reconnaissance).
* **`0xC0000234` (Account Locked Out):** The account has exceeded the lockout threshold configured in Group Policy.

---

## 6. The 60-Day Step-by-Step Transition & Interview-Readiness Plan

```
┌────────────────────────────────────────────────────────┐
│ Weeks 1–2: Protocol & Operating System Internals       │
│ TCP/IP, DNS, HTTP/S, Windows Event Logs, Linux CLI     │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Weeks 3–4: Hands-On Attack-to-Detection Lab Pipeline   │
│ Install Sysmon, simulate brute force with Kali, tune   │
│ custom detection rules in Wazuh / Splunk               │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Weeks 5–6: Scenario Simulation & Incident Reports      │
│ Master the 6 core scenarios; publish 2 formal incident │
│ reports with MITRE ATT&CK mapping to GitHub            │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ Weeks 7–8: Targeted Applications & Mock Interviews     │
│ Apply to IAM Analyst & L1 SOC roles in Hyd / Blr;      │
│ rehearse the "Designer-to-Cyber" script                │
└────────────────────────────────────────────────────────┘
```

---

## 7. How to Answer: "Why Are You Switching from Design?"

When interviewers ask: *"You have a design background and a non-engineering degree. Why are you switching to cybersecurity?"*

**The Exact Script to Deliver:**
> *"That's a very fair question, but in practice, design and cybersecurity solve the exact same core problem: **human behavior, cognitive friction, and system usability**.
> 
> According to global breach reports, over 74% of enterprise security incidents involve human error—phishing, social engineering, credential reuse, and configuration mistakes. Attackers rarely 'hack' firewalls; they manipulate human mental models and habituation.
> 
> In my design career, my entire job was analyzing user journeys, anticipating where users make mistakes, and designing workflows to prevent friction. When I transitioned into IT administration and security operations, that exact analytical mindset translated directly into **threat modeling, identifying abuse cases, and investigating anomaly alerts**. 
> 
> Rather than viewing security as disconnected command lines, I look at security telemetry as a sequence of human and automated behaviors. Combined with my hands-on experience managing Active Directory, firewall rules, and endpoint patching at SansBornes Aerospace, and investigating real-world alerts in my Wazuh SIEM lab and LetsDefend, I bring both operational discipline and human risk analysis to the team."*

---

## 8. Repository Structure & Detailed Playbooks

This repository is maintained on branch `arena/c7ec6ca7-design-to-cyber` and contains dedicated guides:
* **`README.md`** (This file): Master roadmap, lab blueprints, and core concepts.
* **`INTERVIEW_MASTER_PLAYBOOK.md`**: Word-for-word answer scripts, deep-dive scenario triage frameworks, and Windows event log reference cards.
* **`FAST_TRACK_SPRINT.md`**: 90-day application and lateral transition strategy for Hyderabad and Bengaluru tech hubs.
