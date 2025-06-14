# DLP-BGP-IAM Threat Simulation Project

This project simulates insider threat scenarios by integrating:

* **Data Loss Prevention (DLP)** using Wazuh
* **Identity and Access Management (IAM)** using Keycloak
* **BGP Hijack Detection** using BGPalerter

---

## 🚀 Project Summary

Simulates real-world attacks where:

* A user attempts to exfiltrate sensitive data (DLP event)
* A misconfigured IAM policy allows elevated access
* Anomalous BGP route detected representing a network-level threat

Each scenario is documented with logs, screenshots, and tool configurations to demonstrate analyst workflow.

---

## 🔧 Tools Used

| Tool       | Purpose                             | Link                                                                         |
| ---------- | ----------------------------------- | ---------------------------------------------------------------------------- |
| Wazuh      | Host-based alerting & DLP detection | [https://wazuh.com/](https://wazuh.com/)                                     |
| Keycloak   | IAM role & policy testing           | [https://www.keycloak.org/](https://www.keycloak.org/)                       |
| BGPalerter | BGP hijack monitoring               | [https://github.com/nttgin/BGPalerter](https://github.com/nttgin/BGPalerter) |

---

## 📁 Project Structure

```
/DLP-BGP-IAM-Threat-Project
│
├── /DLP
│   ├── wazuh-dlp-rule.conf
│   └── sample-dlp-alert.log
│
├── /IAM
│   ├── keycloak-policy.json
│   └── privilege-violation.log
│
├── /BGP
│   ├── bgpalerter.conf.yml
│   └── hijack-alert.log
│
└── /docs
    └── project-summary.md
```

---

## 📄 Sample Logs

### 🔴 DLP Log

```
2025-06-01 14:34:02 | ALERT | File Transfer Detected: Employee_SSNs.docx | User: intern-usr01 | Action: Blocked
```

### 🔵 IAM Log

```
2025-06-01 15:12:48 | POLICY BREACH | User: intern-usr01 | Escalated Access to Resource: Admin_DB | Result: Unauthorized Access
```

### 🟢 BGP Log

```
2025-06-01 16:27:13 | ALERT | Possible BGP Hijack Detected | Prefix: 192.0.2.0/24 | AS Path: AS64501 > AS12345 (Unexpected)
```

---

## 🛠️ How to Run

1. Clone the repo to your local machine
2. Setup VMs or containers for Wazuh, Keycloak, and BGPalerter
3. Import config files from the respective folders
4. Simulate threat behavior and monitor the logs
5. Document your analysis as a report for portfolio or GitHub Pages

---

## 🧠 What to Highlight in Interviews

* Created threat detection labs simulating insider misuse and external hijack risks
* Demonstrated alert triage, policy misconfiguration, and detection engineering
* Integrated logging, governance, and routing intelligence in one scenario

---

## 📌 Tags

`#DLP` `#IAM` `#BGP` `#Cybersecurity` `#ThreatHunting` `#SOC` `#SIEM` `#InsiderThreat`

---

## 👨‍💻 Author

Designed and simulated by a cybersecurity analyst with hands-on skills in SIEM, IAM policy testing, and open-source threat tools.

> “Detect the invisible. Govern the unknown. Defend beyond the firewall.”
