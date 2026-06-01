# Lab 1 — Brute Force Detection with Wazuh

## Objective
Simulate a brute force attack and detect it using Wazuh SIEM.

## Environment
- Attacker: Kali Linux
- Target: Windows 10 (DESKTOP-EGCVVNJ)
- SIEM: Wazuh + OpenSearch Dashboard

## Steps Performed

### 1. Generated Failed Logins
Triggered 5 consecutive failed login attempts on
Windows endpoint against Administrator account
using lock screen method.

### 2. Alert Observed
| Field | Value |
|---|---|
| Rule ID | 60122 |
| Description | Logon Failure — Unknown user or bad password |
| Level | 5 (Medium) |
| Agent | DESKTOP-EGCVVNJ |
| Count | 5 alerts in 28 seconds |

### 3. Raw JSON Analysis
| Field | Value | Meaning |
|---|---|---|
| targetUserName | Administrator | Account targeted |
| logonType | 2 | Interactive login |
| ipAddress | ::1 | Localhost — local origin |
| subStatus | 0xc000006d | Wrong password |
| eventID | 4625 | Failed logon |

### 4. Triage Report
