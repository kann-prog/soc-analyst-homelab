# Module 1 — SIEM Fundamentals & Alert Triage

## Lab Exercise Completed
- Deployed Wazuh agent on Windows 10 endpoint
- Generated brute force alerts (Rule 60122)
- Triaged alert using 3-question method
- Identified Event ID 4625 in raw JSON

## Triage Report
- Alert: Rule 60122 — Logon Failure
- Event ID: 4625
- Source IP: ::1 (localhost)
- Logon Type: 2 (interactive)
- Verdict: False Positive — authorized lab test
- Action: Ticket closed

## MITRE Mapping
- T1110 — Brute Force
