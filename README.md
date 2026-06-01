# SOC Analyst Home Lab

![Blue Team](https://img.shields.io/badge/Focus-Blue%20Team-blue)
![SIEM](https://img.shields.io/badge/Tool-Wazuh%20SIEM-green)
![Splunk](https://img.shields.io/badge/Tool-Splunk-orange)

## Overview
Hands-on SOC Analyst lab built to develop real-world blue team skills.
All exercises performed on personal virtual machines — no simulations.

**Author:** Kiran V  
**Role Target:** L1 SOC Analyst  
**Location:** Bangalore, India

---

## Lab Environment

| VM | OS | Role |
|---|---|---|
| SOC-SIEM | Ubuntu | Wazuh Server + Splunk |
| Windows-SOC | Windows 10 | Monitored Endpoint |
| Kali Linux | Kali Rolling | Analyst + Attacker Machine |
| Metasploitable2 | Ubuntu 8.04 | Vulnerable Target |

---

## Modules Completed

| Module | Topic | Status |
|---|---|---|
| 1 | SIEM Fundamentals & Alert Triage | ✅ |
| 2 | Wazuh Rules & Decoders | ✅ |
| 3 | Incident Investigation | ✅ |
| 4 | Threat Intelligence & MITRE ATT&CK | ✅ |
| 5 | SIEM Use Cases & SOC Workflows | ✅ |

---

## Hands-On Labs

| Lab | Tools | MITRE |
|---|---|---|
| Brute Force Detection | Wazuh, Windows Event Logs | T1110 |
| Network Packet Analysis | Wireshark | T1046 |
| Port Scanning & OS Fingerprinting | Nmap | T1046 |
| Remote Code Execution via CVE-2011-2523 | Metasploit, Wireshark | T1190 |
| Log Analysis with SPL | Splunk | - |

---

## Skills Demonstrated
- SIEM alert triage (Wazuh + Splunk)
- Windows Event ID analysis (4625, 4624, 4688, 4720)
- Network packet analysis (Wireshark)
- Vulnerability scanning (Nmap NSE)
- Exploitation & post-exploitation analysis
- MITRE ATT&CK mapping
- SPL queries for threat detection
- Incident triage reports

---

## Tools Used
Wazuh | Splunk | Wireshark | Nmap | Metasploit | Kali Linux | VirtualBox
