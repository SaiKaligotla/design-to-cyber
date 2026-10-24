# Sai Kaligotla: Fast-Track Cybersecurity Transition Blueprint

[![Profile](https://img.shields.io/badge/Profile-IT%20Admin%20%2B%20Security%20Labs%20%2B%20Product%20Design-blue.svg)](#)
[![Target Hubs](https://img.shields.io/badge/Location-Hyderabad%20%7C%20Bengaluru%20(Open%20to%2024x7%20Shifts)-orange.svg)](#)
[![Primary Targets](https://img.shields.io/badge/Target%20Roles-IAM%20Analyst%20%7C%20L1%20SOC%20%7C%20Cyber%20Product%20Design-brightgreen.svg)](#)
[![Budget](https://img.shields.io/badge/Budget-%E2%82%B90%20(Free--First)-purple.svg)](#)

A tactical, reality-based transition roadmap built directly from **Sai Kaligotla's verified resume**, current operational experience at **SansBornes Aerospace**, and existing security lab work (Wazuh, LetsDefend, Google Cybersecurity Certificate).

---

## 1. Resume Reality: Your True Market Positioning in India

You are **not** an outsider trying to convince an Indian HR recruiter to take a risk on a non-tech designer. Your resume already gives you an exceptional hybrid profile:

1. **Active IT Admin Experience on Your Resume:**
   - **Role:** *IT Administrator — Endpoint Security & Access Management* at *SansBornes Aerospace Pvt. Ltd.* (Bengaluru, Mar 2025 – Present).
   - **Proven Responsibilities:** Sole IT owner for a 15-person aerospace engineering firm managing 20+ endpoints, Active Directory, Group Policy, RBAC, least privilege, joiner/mover/leaver provisioning/deprovisioning, patching, antivirus, LAN/Wi-Fi, DNS, DHCP, firewall rules, backups, and audit-ready documentation.
2. **Proven Security Operations Practice:**
   - **Wazuh SIEM/EDR Lab:** Kali Linux, Ubuntu Server, Wazuh agent deployment, SSH brute force simulation, escalation notes.
   - **LetsDefend Simulated SOC:** 30+ simulated phishing, endpoint, and anomalous login alerts; 4 formal incident reports (3 true positive, 1 false positive) with VirusTotal and URLScan validation.
   - **Forage Simulations:** Mastercard Cyber (phishing awareness) and Deloitte Cyber (web log pattern analysis).
3. **Validated Credentials & Flexibility:**
   - **Google Cybersecurity Professional Certificate** (Coursera, 2026).
   - **Google Data Analytics Certificate** (Coursera, 2023).
   - Based in **Hyderabad / Bengaluru**, immediate joiner, and explicitly **comfortable with 24x7 rotational shifts**.

---

## 2. The 3 Fastest Job Targets (Hyderabad & Bengaluru)

| Target Role | Why You Are an Immediate Match | Target Employers (Hyd / Blr) | Expected Salary (India) | Time to Placement |
| :--- | :--- | :--- | :--- | :--- |
| **1. IAM Operations Analyst / Access Governance Associate** *(Fastest & Highest Fit)* | You are **already performing user lifecycle management** (joiner/mover/leaver, provisioning, deprovisioning, RBAC, Active Directory, least privilege) at SansBornes Aerospace. | Microland, Grant Thornton, HCLTech, Caterpillar, i-Admin, Mattel, PepsiCo, Deloitte, Cognizant | **₹5.0 – ₹8.5 LPA** | **3 to 6 Weeks** |
| **2. L1 SOC Analyst / Incident Triage Analyst** | You have real IT Admin infrastructure experience + Wazuh lab + LetsDefend 30+ alert reports + Google Cyber Cert + open to 24x7 rotational shifts. | Revantage, Informica, UST, Zelis, Sequretek, Inspira Enterprise, Netenrich, MoonPay, Wipro CyberShield | **₹4.5 – ₹7.5 LPA** | **4 to 8 Weeks** |
| **3. Product Designer — Cyber / Enterprise SaaS** *(The High-Salary Hybrid Play)* | You have 3+ years of elite UI/UX design (Figma, research, systems) **PLUS** you actually understand SIEM alerts, IT admin workflows, and security tooling. | Quick Heal/Seqrite, Sequretek, CloudSEK, Zscaler, CrowdStrike, Sophos, BrowserStack | **₹12 – ₹18+ LPA** | **6 to 10 Weeks** |

---

## 3. Why "Just Viewing Windows Logs" Doesn't Make Sense (And The Real Lab)

Simply opening `eventvwr.msc` and looking at Event ID 4625 is passive theory. In an Indian technical interview for an L1 SOC or SecOps role, interviewers will challenge you:
> *"Walk me through an alert you investigated from start to finish: How was the attack generated? What telemetry was collected? What rule fired? How did you verify whether it was a True Positive or False Positive? What containment action did you take?"*

### The Complete 5-Stage Detection & Triage Lab (100% Free on Windows 11)

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

#### Stage 1: The Telemetry Pipeline (Sysmon + Windows Event Viewer)
* **The Flaw of Default Windows Logging:** Default Windows Security logs only tell you *who* logged in (4624/4625), but not *what process* ran or what external IP it connected to.
* **The Fix:** Download and install Microsoft's free **Sysmon (System Monitor)** with the industry-standard **SwiftOnSecurity configuration**:
  * **Event ID 1:** Process Creation (captures the full command line, parent process, hashes).
  * **Event ID 3:** Network Connection (captures source/destination IP, port, initiating process).
  * **Event ID 11:** File Create (detects ransomware or dropped malware).

#### Stage 2: Attack Simulation (Kali Linux Host-Only VM)
* Use your Kali VM inside VirtualBox / VMware Workstation Pro (Host-Only Network):
  1. **Brute Force Simulation:** Run `hydra -l administrator -P /usr/share/wordlists/rockyou.txt ssh://<Linux_IP>` or RDP brute force against Windows.
  2. **LOLBAS Execution (Living off the Land):** Run encoded PowerShell commands on the target machine simulating an attacker downloading a payload:
     ```powershell
     powershell.exe -ExecutionPolicy Bypass -WindowStyle Hidden -Command "Write-Output 'Simulated Malware Trigger'"
     ```

#### Stage 3: Ingestion & Alert Rule Tuning in Wazuh / Splunk
* In your Wazuh Manager:
  * Check the alert trigger under `/var/ossec/logs/alerts/alerts.json`.
  * Open `/var/ossec/etc/rules/local_rules.xml` and write a custom detection rule (e.g., alert level 10 when 5 failed logons occur in 60 seconds from the same IP).
* In Splunk (Free 500MB/day license):
  * Write the SPL search query:
    ```spl
    index=windows (EventCode=4625 OR EventCode=1)
    | stats count by user, src_ip, Image, CommandLine
    | where count > 3
    ```

#### Stage 4: Triage, Indicator Enrichment & Report Writing
* Pull the suspicious IP / domain / hash and enrich it using **VirusTotal, URLScan, and AbuseIPDB**.
* Determine: **True Positive** (authorized test) vs **False Positive** (benign software glitch).
* Document in an incident report following the **NIST SP 800-61** lifecycle:
  1. *Detection & Analysis:* Summary of alert, affected host, user account, timestamp.
  2. *Containment:* Host isolation, firewall rule block (`ufw deny from <Attacker_IP>`), account lockout.
  3. *Remediation & Lessons Learned:* Enforce account lockout threshold via Group Policy (GPO); enable number-matching MFA.

---

## 4. The 30-Day Execution Plan to Land Offers

### Week 1: Resume Calibration (IAM & SOC Focus)
* Update your resume headline to:
  `IT Systems & Security Administrator | Identity & Access Management (IAM), Endpoint Security & SOC Analysis`
* Put your current role at **SansBornes Aerospace** front and center:
  * Emphasize: *Active Directory user lifecycle (joiner/mover/leaver), RBAC, GPO, patch management, endpoint security, firewall administration.*
  * Feature your **Wazuh & LetsDefend investigations** as bulleted proof of work.

### Week 2: Build the GitHub "Proof-of-Work" Lab Repository
* Clean up your GitHub repository (`SaiKaligotla/design-to-cyber`):
  * Publish 2 detailed markdown writeups:
    1. *Wazuh SIEM Deployment & SSH Brute-Force Detection Walkthrough* (with screenshots, log snippets, and local rule configurations).
    2. *LetsDefend Phishing & Endpoint Triage Case Study* (detailing your 4 formal incident reports and IOC checks).
* Add your GitHub link directly beneath your contact info on your resume.

### Weeks 3–4: Targeted Application Blitz (Hyderabad & Bengaluru)
* Apply to 15–20 openings per week on **LinkedIn India, Instahyre, and Foundit**:
  * **Search Query 1:** `"IAM Analyst" OR "Identity Access Management" (Hyderabad OR Bengaluru)`
  * **Search Query 2:** `"L1 SOC" OR "Security Operations Analyst" (Hyderabad OR Bengaluru)`
  * **Search Query 3:** `"IT Security Administrator"`
* Reach out to recruiters and team leads directly on LinkedIn:
  > *"Hi [Name], I'm currently the sole IT Administrator at SansBornes Aerospace managing Active Directory, RBAC, and endpoint security. I have hands-on Wazuh and LetsDefend SOC triage experience, hold the Google Cybersecurity Certificate, and am based in Hyderabad/Bengaluru available for immediate joining across 24x7 rotational shifts. Would love to be considered for open IAM / SOC Analyst roles on your team: [Resume/GitHub Link]."*
