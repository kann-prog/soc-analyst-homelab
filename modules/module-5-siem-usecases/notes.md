# Module 5 — SIEM Use Cases & SOC Workflows

## What is a Use Case
A documented detection scenario that tells the SIEM what
to look for, what rule to fire, and what action to take.

## Core SOC Use Cases
| Use Case | Event IDs |
|---|---|
| Brute Force | 4625 x5 fast |
| Password Spray | 4625 different accounts slow |
| Account Compromise | 4625 then 4624 |
| Privilege Escalation | 4732 |
| New Account Created | 4720 |
| Lateral Movement | 4648 |
| Persistence via Task | 4698 |
| Malware Execution | 4688 |
| Ransomware | Mass syscheck alerts |

## Log Types
- Windows Security Log: Auth events, account changes
- Syslog: Linux auth, kernel, application events
- Firewall Log: Allowed/blocked connections
- DNS Log: Domain lookups — detects C2
- Proxy Log: URLs visited, user agents

## Linux Log Locations
- /var/log/auth.log — SSH, sudo, authentication
- /var/log/syslog — General system events
- /var/log/kern.log — Kernel messages
- /var/log/apache2/access.log — Web server access

## Log Correlation
Combining events from multiple log sources to build
a complete picture of an attack. No single log tells
the full story.

## SOC Shift Workflow
1. Handover from previous analyst
2. Check dashboard — any P1/P2 open
3. Triage alerts oldest first
4. Document each — close FP, escalate TP
5. Run threat intel checks (VirusTotal, AbuseIPDB)
6. Update open tickets
7. End of shift handover notes

## Alert Fatigue
When high alert volume causes analysts to miss real threats.
Wazuh prevents it through frequency rules, severity levels,
and alert grouping.

## SOC Metrics
- MTTD: Mean Time to Detect
- MTTR: Mean Time to Respond
- False Positive Rate
- Alert Volume
- Escalation Rate
