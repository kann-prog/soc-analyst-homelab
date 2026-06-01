# Module 4 — Threat Intelligence & MITRE ATT&CK

## What is Threat Intelligence
Information about known attackers, tools, techniques used
to detect and prevent attacks.

## 3 Types
- Strategic: High level for management
- Tactical: Attacker techniques and tools
- Operational: Specific IOCs of active attack

## IOCs (Indicators of Compromise)
Evidence that an attack has occurred or is occurring.

| Type | Example | Wazuh Field |
|---|---|---|
| IP Address | 185.220.101.45 | data.srcip |
| File Hash | abc123def456 | Integrity monitoring |
| Domain | malware-c2.ru | DNS query logs |
| File Path | C:\Users\Public\evil.exe | Syscheck alerts |

## MITRE ATT&CK
Publicly available knowledge base of real attacker TTPs.
Every Wazuh rule maps to a MITRE technique.
Website: attack.mitre.org

## 14 Tactics (Attack Lifecycle)
1. Reconnaissance
2. Resource Development
3. Initial Access
4. Execution
5. Persistence
6. Privilege Escalation
7. Defense Evasion
8. Credential Access
9. Discovery
10. Lateral Movement
11. Collection
12. Command & Control
13. Exfiltration
14. Impact

## Key Techniques
- T1110: Brute Force
- T1078: Valid Accounts
- T1136: Create Account
- T1053: Scheduled Task
- T1046: Network Service Scanning
- T1190: Exploit Public Facing Application

## Threat Intel Feeds
- VirusTotal: File hash, URL, IP reputation
- AbuseIPDB: Malicious IP reports
- AlienVault OTX: Full IOC feeds
- Talos Intelligence: Cisco threat intel

## Threat Hunting
Proactively searching for threats that haven't triggered
an alert yet, using MITRE ATT&CK to predict attacker next
steps and hunting for evidence before alert fires.

## Ransomware MITRE Chain
- T1566 Initial Access — phishing
- T1059 Execution — malicious script
- T1053 Persistence — scheduled task
- T1110 Credential Access — brute force
- T1021 Lateral Movement — file server
- T1486 Impact — encrypts files
