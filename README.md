# 🧠 Cybersecurity Incident Response – 2025 🛡️

This repository documents a hands-on incident response walkthrough simulating a real-world security incident on a Windows workstation. It follows the full IR lifecycle using NIST and SANS frameworks, from preparation to post-incident actions.

> _“Keep learning, keep adapting, and keep growing.”_ – Cyb3rd4nc3

---

## 📚 Table of Contents

- [Overview](#overview)
- [Frameworks Used](#frameworks-used)
- [IR Lifecycle Walkthrough](#ir-lifecycle-walkthrough)
- [Technical Tools & Commands](#technical-tools--commands)
- [Indicators of Compromise (IOCs)](#indicators-of-compromise-iocs)
- [Screenshots](#screenshots)
- [Lessons Learned](#lessons-learned)
- [About Me](#about-me)

---

## 📌 Overview

This lab simulates a real-world incident triggered by suspicious system behavior, reported by a user and escalated to the SOC. We analyze a malicious `.docm` file leading to a C2 connection and persistent process injection.

---

## 📐 Frameworks Used

| Framework | Phases |
|----------|--------|
| **NIST** | Prep → Detect/Analyze → Contain → Eradicate → Recover → Post-Incident |
| **SANS** | Prep → Identification → Containment → Eradication → Recovery → Lessons Learned |

---

## 🔍 IR Lifecycle Walkthrough

### 🛠️ Preparation
- Setup IR policies and procedures
- Deployed SIEM & EDR tools
- Conducted risk assessment & tabletop exercises

### ⚠️ Detection & Analysis
- Identified high CPU process: `3d33es454e.exe`
- Connection to C2: `45.33.32.156:42424`
- Malicious macro doc: `invoice n. 37484567 (1).docm`
- Analyzed VBA code for behavior

### 🔒 Containment
- Network isolation of infected host
- Process termination via Task Manager
- IOC block via EDR/SIEM rules

### 🧹 Eradication
- Deleted malware and macro file
- Cleaned registry persistence key

### ♻️ Recovery
- Restored clean system image
- Verified system integrity and logs

### 📄 Post-Incident
- Documented steps, IOCs, and lessons
- Updated playbooks and tooling
- Conducted internal IR review

---

## 🧰 Technical Tools & Commands

```bash
# Identify malicious process outbound connection
netstat -aofn | find "4400"

# Investigate macros
Menu > View > Macros > Edit
```
## License
This project follows the [MIT License](LICENSE).

## Author
**Daniel M. Mwithui**  
[LinkedIn](https://www.linkedin.com/in/daniel-mwendwa-mwithui/) | [GitHub](https://github.com/daniel-mwendwa)


