# SOC Analyst Home Lab & SIEM Project
This repository contains a full end-to-end **Security Operations (SOC) Analyst Lab** built using **Wazuh SIEM**, Windows & Linux endpoints, Sysmon, simulated attack scenarios, and custom detection rules. The project is designed to demonstrate practical SOC skills including log collection, threat detection, alerting, incident analysis, and automated response.

---

## Overview
This project replicates a small SOC environment using free and open-source tools. It includes:

* A full Wazuh SIEM deployment (Manager, Indexer, Dashboard)
* Windows & Linux endpoints with agents installed
* Sysmon for advanced Windows logging
* Simulated security incidents
* Custom detection rules
* Incident reports for investigations
* Automation scripts for alert responses

This project is ideal for SOC Analyst and Cybersecurity Analyst.

---

## Project Goals
* Understand real-world SIEM usage and alert workflows
* Collect and store logs from multiple systems
* Create and tune detection rules
* Simulate realistic attacks for analysis
* Produce professional incident reports

---

## Architecture
```
[Windows/Linux Endpoints]
        ↓ (logs)
    [Wazuh Agent]
        ↓
    [Wazuh Manager] → applies rules
        ↓
    [Wazuh Indexer] → stores events
        ↓
    [Wazuh Dashboard] → displays alerts & logs
```

---

## Tools Used
* **Wazuh SIEM** – log collection, detection rules, dashboard
* **Elastic Stack (Wazuh Indexer)** – log indexing & storage
* **Windows 11 Laptop** – endpoint monitoring
* **Linux VM (Ubuntu)** – server & attacker machine
* **Sysmon** – advanced Windows logging
* **SwiftOnSecurity Sysmon Config** – clean & security-focused config
* **Python / PowerShell** – alert automations
* **VirtualBox** – virtualization environment

---

## Attack Scenarios Simulated
This project includes step-by-step recreations of realistic threats:

### 1. SSH Brute Force Attack
* Multiple failed SSH login attempts
* Detected using authentication logs

### 2. Malicious PowerShell Download
* Remote download of suspicious file
* Triggers Sysmon Event ID 1, 3, and 11

### 3. EICAR Malware Test
* Safe malware test file to trigger AV + SIEM alerts

### 4. Suspicious Process Tree
```
cmd.exe → powershell.exe → curl.exe → malware.exe
```

---

## Custom Detection Rules
This repo includes examples such as:
* SSH brute-force detection rule
* PowerShell download detection rule
* Suspicious process creation rule

---

## Repository Structure (WIP)
```
.
├── README.md
├── architecture/
├── attack-scenarios/
├── configs/
├── detection-rules/
├── incident-reports/
└── scripts/
```

- `architecture`: diagrams and deployment notes
- `attack-scenarios`: step-by-step simulated attacks used for testing
- `configs`: example configuration files and helper scripts
- `detection-rules`: Wazuh/ELK rule examples for detections
- `incident-reports`: SOC-style investigation writeups for scenarios
- `scripts`: automation and test scripts (PowerShell, shell)

---

## Incident Reports
Each simulated attack includes a full SOC-style investigation with:
* Event timeline
* Indicators of Compromise
* SIEM alerts & log samples
* Root cause analysis
* Containment & remediation steps

These reports demonstrate real SOC workflow and decision-making.

---

## How to Use This Repo (WIP)
1. Clone the repo


---

## Why This Project Is Valuable
* Shows real hands-on SOC skills
* Demonstrates SIEM knowledge
* Includes incident reports for interviews
* Portfolio project for cybersecurity roles
