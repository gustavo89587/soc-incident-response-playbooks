# SOC Incident Response Playbooks

This repository contains **practical SOC incident response playbooks** designed to support
real-world alert triage, investigation, decision-making, and response.

The focus is not on tools, but on **how a SOC analyst thinks and acts** when an alert appears.

> Alert ≠ Incident  
> Context + Evidence = Decision

---

## 🎯 Purpose

These playbooks aim to:
- Standardize SOC triage and response workflows
- Reduce false positives and alert fatigue
- Improve consistency in incident handling
- Demonstrate evidence-based decision making
- Support junior → mid SOC analyst growth

Each playbook follows a **repeatable and auditable process** aligned with SOC best practices.

---

## 🧠 Decision Model Used

All playbooks classify alerts as one of the following:

- **False Positive (FP)**  
  Alert triggered by a security tool, but evidence proves the activity is legitimate.

- **True Positive (TP)**  
  Evidence confirms malicious activity and an actual security incident.

- **Benign True Positive (BTP)**  
  Behavior looks suspicious or malicious, but is **authorized and expected** in the environment
  (e.g., admin activity, security tools, automation).

---

## 📂 Repository Structure

soc-incident-response-playbooks/
│
├── playbooks/
│ ├── brute-force-credential-access/
│ │ └── README.md
│ │
│ ├── suspicious-powershell-execution/
│ │ └── README.md
│ │
│ ├── lolbin-abuse/
│ │ └── README.md
│ │
│ ├── malware-alert-triage/
│ │ └── README.md
│ │
│ └── phishing-token-abuse/
│ └── README.md
│
├── templates/
│ ├── triage-checklist.md
│ ├── incident-timeline.md
│ └── incident-report-template.md
│
├── queries/
│ ├── generic-authentication-queries.md
│ ├── powershell-hunting.md
│ └── endpoint-behavior-queries.md


---

## 🧪 Playbooks Overview

### 1️⃣ Brute Force / Credential Access
- Multiple failed logins followed by success
- External IPs, unusual login times
- Password spraying and brute force indicators
- Identity and authentication abuse

### 2️⃣ Suspicious PowerShell Execution
- Encoded commands
- Office → PowerShell execution chains
- Living-off-the-land behavior
- Script-based post-exploitation indicators

### 3️⃣ LOLBin Abuse
- `mshta.exe`, `rundll32.exe`, `regsvr32.exe`, etc.
- Execution from unusual parent processes
- External content execution
- EDR-blocked but high-risk behaviors

### 4️⃣ Malware Alert Triage
- Antivirus / EDR detections
- Validation of severity and scope
- False positive vs real infection analysis
- Containment and eradication decisions

### 5️⃣ Phishing & Token Abuse
- Suspicious email activity
- OAuth / token misuse
- MFA fatigue scenarios
- Account compromise indicators

---

## 🧭 Standard Playbook Format

Each playbook follows the same structure:

- **Incident Scenario**  
  What triggered the alert?

- **Detection**  
  How the alert was generated and which signals were involved.

- **Analysis**  
  Evidence review, alternative hypotheses, and context validation.

- **Risk Assessment**  
  Potential impact if the activity is malicious.

- **Response Actions**  
  Step-by-step response, focusing on containment with minimal disruption.

- **MITRE ATT&CK Mapping**  
  Relevant tactics and techniques.

- **Lessons Learned**  
  Detection improvements and operational insights.

---

## 🛡️ SOC Principles Applied

- Sequence over single events
- Context over severity score
- Evidence before escalation
- Containment with control, not panic
- Documentation is part of the response

---

## 👤 Author

**Gustavo Okamoto**  
Cybersecurity Analyst — SOC / SIEM / Incident Response  

- GitHub: https://github.com/gustavo89587  
- LinkedIn: https://www.linkedin.com/in/gustavo-okamoto-de-carvalho-ti

---

## 📌 Disclaimer

All scenarios are **lab-based or simulated**, inspired by real-world SOC operations.
No sensitive or proprietary data is included.



