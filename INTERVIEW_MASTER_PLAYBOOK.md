# The Cybersecurity Interview Master Playbook (Designer & Non-Tech Edition)

> **Core Objective:** Bridge the gap between theoretical certifications and operational technical interviews in India. Designed specifically for designers, career-switchers, and non-tech candidates who get rejected at the scenario-based interview stage.

---

## Table of Contents
1. [The 5 Hidden Traps Where Non-Tech Switchers Fail Interviews](#1-the-5-hidden-traps-where-non-tech-switchers-fail-interviews)
2. [The 5-Step Incident Triage Response Framework](#2-the-5-step-incident-triage-response-framework)
3. [The 6 Real-World Interview Scenarios & Exact Answer Scripts](#3-the-6-real-world-interview-scenarios--exact-answer-scripts)
   - [Scenario 1: Brute Force (Failed Logins Followed by a Success)](#scenario-1-brute-force-failed-logins-followed-by-a-success)
   - [Scenario 2: Phishing Investigation & Raw Header Analysis](#scenario-2-phishing-investigation--raw-header-analysis)
   - [Scenario 3: Impossible Travel / Compromised Cloud Account](#scenario-3-impossible-travel--compromised-cloud-account)
   - [Scenario 4: Potential Ransomware / Malicious Process Execution](#scenario-4-potential-ransomware--malicious-process-execution)
   - [Scenario 5: The "Service Account Alert" Trap](#scenario-5-the-service-account-alert-trap)
   - [Scenario 6: Active Directory Privilege Escalation](#scenario-6-active-directory-privilege-escalation)
4. [Windows Event Log Deep Dive (Beyond Event ID 4625)](#4-windows-event-log-deep-dive-beyond-event-id-4625)
5. [The "Why Are You Switching from Design?" Killer Answer Script](#5-the-why-are-you-switching-from-design-killer-answer-script)

---

## 1. The 5 Hidden Traps Where Non-Tech Switchers Fail Interviews

| Interview Trap | What the Candidate Does (Fails) | What the Interviewer is Actually Testing | The Winning Approach |
| :--- | :--- | :--- | :--- |
| **Trap 1: The Definition Reciter** | Recites textbook definitions when asked a scenario: *"Brute force is when an attacker tries many passwords until they succeed."* | Can this candidate handle a real security ticket on their own without breaking systems? | Answer using a structured 5-step operational framework: **Scope → Enrich → Contain → Eradicate → Document**. |
| **Trap 2: The Surface Log Trap** | Memorizes only `Event ID 4625 = Failed Logon`. Cannot explain **Logon Types** (Type 2 vs 3 vs 10) or **Sub-status Codes** (`0xC000006A` vs `0xC0000064`). | Did the candidate actually investigate incidents, or did they just watch video tutorials? | Master the sub-fields: Logon Type tells you the attack vector; sub-status code tells you if the attacker is guessing passwords or enumerating usernames. |
| **Trap 3: The Phishing Surface Trap** | *"I check if the email link looks strange and run it through VirusTotal."* | Do they understand email delivery architecture (RFC 822 headers, authentication protocols, and mail flow)? | Inspect raw headers: **Envelope Sender (`Return-Path`) vs Display Sender (`From`)**, `Received` hops, and **SPF/DKIM/DMARC** authentication results. |
| **Trap 4: The Blast Radius Trap** | *"The server is infected! I will immediately pull the power plug / reboot the machine!"* | Do they understand incident handling hygiene? (Powering off destroys live volatile memory RAM containing encryption keys and running processes). | **Never power off an infected machine.** Isolate the host from the network (physically or via EDR host isolation) to preserve memory artifacts for digital forensics. |
| **Trap 5: The Apologetic Designer Syndrome** | Apologizes for their design background: *"I don't have an engineering degree, but I am passionate and learning fast."* | Does this candidate have conviction and unique problem-solving capabilities? | Frame design as an **analytical superpower**: Over 74% of breaches exploit human error and friction. Designers understand cognitive psychology, abuse cases, and workflow vulnerabilities. |

---

## 2. The 5-Step Incident Triage Response Framework

Whenever an interviewer asks a scenario starting with *"You see an alert for X, what do you do?"*, structure your response in this exact sequence:

```
┌────────────────────────────────────────────────────────┐
│ 1. SCOPE & VALIDATE (Confirm True vs False Positive)   │
│ Time, user, hostname, source IP, baseline behavior     │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ 2. ENRICH & CORRELATE (Gather Context & Threat Intel)  │
│ SIEM logs, Sysmon, EDR, VirusTotal, URLScan, AbuseIPDB │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ 3. CONTAIN (Stop the Blast Radius)                     │
│ Network isolation, revoke tokens, reset passwords      │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ 4. ERADICATE & RECOVER (Remove Threat & Restore Ops)   │
│ Kill process, delete persistence (run keys/tasks)      │
└──────────────────────────┬─────────────────────────────┘
                           │
┌──────────────────────────▼─────────────────────────────┐
│ 5. DOCUMENT & HARDEN (Lessons Learned / Root Cause)    │
│ Incident ticket, MITRE ATT&CK mapping, rule tuning     │
└────────────────────────────────────────────────────────┘
```

---

## 3. The 6 Real-World Interview Scenarios & Exact Answer Scripts

### Scenario 1: Brute Force (Failed Logins Followed by a Success)
**The Question:** *"You see an alert showing 50 failed login attempts on a user account within 3 minutes, followed by a successful login. What do you do?"*

**The Strong Answer Script:**
> *"This pattern indicates an active brute-force or password spraying attack where the adversary successfully guessed the credential. I treat this as an active account compromise.
> 
> 1. **Scope & Validate:** I check the source IP, destination host, and the timestamp. I inspect **Event ID 4625** to determine the **Logon Type**: Is it Type 10 (RDP from an external IP) or Type 3 (SMB/network share)? I check the sub-status code: `0xC000006A` confirms bad password attempts against an existing user.
> 2. **Post-Compromise Activity:** The most critical question is: *What did the session do after the successful Event ID 4624?* I check Sysmon Event ID 1 (Process Creation) and PowerShell logs for abnormal execution (e.g. `whoami`, `net user`, `vssadmin`).
> 3. **Containment:** If the source IP is external or unrecognized, I immediately revoke all active sessions in Azure AD / Entra ID, force a password reset, and temporarily disable the account in Active Directory. If the source IP is external, I block it on the perimeter firewall.
> 4. **Eradication & Forensics:** I verify whether MFA was prompted or bypassed (e.g., MFA fatigue). I check if any new mail forwarding rules or persistence mechanisms (scheduled tasks, new local users) were created.
> 5. **Documentation:** I map this to **MITRE ATT&CK T1110.001 (Password Guessing)** and file a high-severity incident report with IOCs."*

---

### Scenario 2: Phishing Investigation & Raw Header Analysis
**The Question:** *"A user forwards an email claiming to be from the CEO asking to review an urgent PDF invoice. How do you analyze it?"*

**The Strong Answer Script:**
> *"I treat this as suspected Business Email Compromise (BEC) or credential harvesting.
> 
> 1. **Do Not Click:** I do not interact with the email in a standard client. I extract the `.eml` or `.msg` file and examine it in an isolated analysis sandbox.
> 2. **Inspect Raw RFC 822 Headers:**
>    - **Sender Alignment:** I compare the display `From:` address with the envelope sender (`Return-Path:`). Attackers often spoof the display name while the `Return-Path` points to an external adversary domain.
>    - **Authentication Checks:** I inspect the `Authentication-Results` header:
>      - **SPF:** Did the sending mail server IP pass SPF authorization for that domain?
>      - **DKIM:** Is the cryptographic signature valid and aligned?
>      - **DMARC:** Did the email pass DMARC policy validation?
>    - **Received Hops:** I trace the `Received:` headers from bottom to top to identify the originating server IP and MTA path.
> 3. **URL & Attachment Analysis:**
>    - If there is a URL, I defang it (`hxxps[://]...`) and inspect it in **URLScan.io** or **VirusTotal** without visiting it directly.
>    - If there is a PDF attachment, I extract its SHA-256 hash in terminal (`sha256sum invoice.pdf`) and search VirusTotal. I inspect the PDF streams with `pdfid` to check for embedded JavaScript (`/JS`) or launch actions (`/Launch`).
> 4. **Scope Across Organization:** If malicious, I take the `Message-ID` or subject line and query the email gateway (Microsoft Defender for Office 365 / Mimecast) to find how many other employees received it and purge it from all mailboxes.
> 5. **User Communication:** I thank the reporting user, reinforcing good security reporting culture."*

---

### Scenario 3: Impossible Travel / Compromised Cloud Account
**The Question:** *"An alert triggers for user 'Priya' signing in from Bengaluru, and 15 minutes later signing in from Frankfurt, Germany. What do you do?"*

**The Strong Answer Script:**
> *"This is an **Impossible Travel** anomaly—a physical person cannot travel between India and Germany in 15 minutes.
> 
> 1. **Verify Context:** First, I check whether the German IP belongs to a known corporate VPN, an authorized cloud proxy (like Zscaler), or an AWS/Azure datacenter. If the user connected through a corporate VPN egress in Frankfurt, it is a benign false positive.
> 2. **Risk Indicators:** If the German IP belongs to a commercial VPN (NordVPN, ExpressVPN) or a foreign ISP, I treat it as potential session hijacking or credential theft.
> 3. **Session Audit:** I check Azure AD / Entra ID sign-in logs: Was MFA prompted? Was it satisfied? Did the user trigger an MFA fatigue push approval?
> 4. **Containment:** I initiate an immediate **Revoke Sign-In Sessions** action in Microsoft 365, reset the account password, and contact the employee via a secondary out-of-band channel (phone call) to confirm their physical location.
> 5. **Audit Post-Auth Actions:** I check Microsoft Unified Audit Logs for mailbox rule creation (e.g. forward all emails with keyword 'invoice' to an external inbox), new application registrations, or SharePoint bulk file downloads."*

---

### Scenario 4: Potential Ransomware / Malicious Process Execution
**The Question:** *"An alert flags an endpoint executing `vssadmin.exe delete shadows /all /quiet`. What is your immediate reaction?"*

**The Strong Answer Script:**
> *"This is a critical, high-severity alert. Adversaries execute `vssadmin delete shadows` right before deploying ransomware to delete Volume Shadow Copies, preventing the organization from recovering files without paying the ransom.
> 
> 1. **Containment FIRST (Do Not Reboot!):** I immediately initiate **EDR Network Isolation** on that endpoint. This cuts off all network traffic to prevent lateral movement or command-and-control communication while keeping the EDR agent connected. **I do NOT power off the computer**, because shutting it down destroys volatile RAM containing unencrypted keys, running processes, and memory artifacts.
> 2. **Process Tree Investigation:** In EDR/Sysmon, I trace the parent process of `vssadmin.exe`. Was it spawned by `cmd.exe`, `powershell.exe`, or a malicious document like `word.exe`?
> 3. **Identify Executable & Hash:** I identify the root malicious executable, extract its SHA-256 hash, and check for encryption activity (mass file renames or `.locked` extensions).
> 4. **Scope the Fleet:** I search the SIEM/EDR across all endpoints for that parent process hash to verify if other machines are infected.
> 5. **Escalation:** I immediately escalate to the Incident Response Lead, preserve memory dumps, and verify that immutable offline backups are secure."*

---

### Scenario 5: The "Service Account Alert" Trap
**The Question:** *"You see an alert for 500 failed logins in 5 minutes on `svc_sap_sync`. Do you immediately disable the account?"*

**The Winning Answer Script (Bypassing the Trap):**
> *"No, I do **NOT** immediately disable or lock a critical service account without investigation. Disabling a production service account can instantly take down enterprise business operations (such as SAP database synchronization or manufacturing lines), creating a self-inflicted Denial of Service.
> 
> 1. **Identify Source IP:** I check the source IP in the failed logon events. 
>    - In over 80% of corporate environments, a sudden spike in failed logins on a service account is caused by an internal IT misconfiguration: someone rotated the service account password in Active Directory, but forgot to update a scheduled task, Windows service, or script on one server, which keeps retrying with the old cached credentials.
> 2. **Verify Internal vs External:** If the source IP is an internal application server, I check which process is generating the requests and notify the application owner to update the credentials.
> 3. **If Source is Untrusted/Adversary:** If the source IP is unknown, external, or an infected workstation attempting Kerberoasting or password spraying, I contain the **source host** (firewall rule or host isolation) rather than disabling the service account itself, preserving business uptime while neutralizing the threat."*

---

### Scenario 6: Active Directory Privilege Escalation
**The Question:** *"You observe an event indicating a standard helpdesk user was suddenly added to the 'Domain Admins' security group. How do you investigate?"*

**The Strong Answer Script:**
> *"Unauthorized addition to Domain Admins represents critical privilege escalation.
> 
> 1. **Inspect Event ID 4728:** In Windows Event Viewer / Active Directory Security logs, I check **Event ID 4728 (A member was added to a security-enabled global group)**.
> 2. **Identify Who Performed the Action:** In the event details, I examine the **Subject User Name** (the account that executed the change) and the **Member User Name** (the account added).
> 3. **Check Change Management Ticket:** Was there an approved IT Change Request (RFC) or JIRA ticket for temporary elevated access (e.g. PAM / Just-In-Time access)?
> 4. **If Unauthorized:** If no ticket exists, this indicates possible compromise of an existing administrator account (e.g., through Mimikatz Pass-the-Hash or Kerberoasting). I immediately remove the user from the Domain Admins group, revoke Kerberos tickets (`klist purge`), force a password reset on both accounts, and investigate the host where the change was executed."*

---

## 4. Windows Event Log Deep Dive (Beyond Event ID 4625)

To impress technical interviewers, you must speak fluently about the **Logon Types** and **Sub-Status Codes** within Event ID 4625:

### Critical Logon Types in Windows
* **Logon Type 2 (Interactive):** User physically typed credentials at the local keyboard/console.
* **Logon Type 3 (Network):** Connection over the network (e.g., accessing an SMB shared folder, using `PsExec`, or mapping a drive). Very common in lateral movement.
* **Logon Type 4 (Batch):** Scheduled task running under an account's credentials.
* **Logon Type 5 (Service):** A Windows service started by the Service Control Manager.
* **Logon Type 7 (Unlock):** User unlocked a previously locked screen.
* **Logon Type 10 (RemoteInteractive / RDP):** User connected remotely via Remote Desktop Protocol. Crucial for detecting external brute-force attacks against exposed RDP ports.

### Critical Sub-Status Failure Codes
* **`0xC000006A` (Bad Password):** The username exists in the domain/system, but the password provided was wrong. (Indicates password spraying or brute force).
* **`0xC0000064` (User Name does not exist):** The username typed does not exist. (Indicates username enumeration).
* **`0xC000006D` (Bad Credentials):** General logon failure caused by incorrect username or authentication information.
* **`0xC0000234` (Account Locked Out):** The user account has exceeded the lockout threshold set in Group Policy.

---

## 5. The "Why Are You Switching from Design?" Killer Answer Script

When Indian interviewers ask: *"You have 3+ years in design and a non-engineering degree. Why are you switching to cybersecurity? Isn't it completely unrelated?"*

**The Perfect Script:**
> *"That's a fair question, but in practice, design and cybersecurity solve the exact same core problem: **human behavior, cognitive friction, and system usability**.
> 
> According to global breach reports, over 74% of enterprise security breaches involve the human element—phishing, social engineering, credential reuse, and configuration mistakes. Attackers rarely 'hack' firewalls; they manipulate human mental models and habituation.
> 
> In my design career, my entire job was analyzing user journeys, anticipating where users make mistakes, and designing workflows to prevent friction. When I transitioned into IT administration and security operations, that exact analytical mindset translated into **threat modeling, identifying abuse cases, and investigating anomaly alerts**. 
> 
> Rather than viewing security as disconnected command lines, I look at security telemetry as a sequence of human and automated behaviors. Combined with my hands-on experience managing Active Directory, firewall rules, and endpoint patching at SansBornes Aerospace, and investigating 30+ real-world alerts on LetsDefend and Wazuh, I bring both operational discipline and human risk analysis to the SOC."*
