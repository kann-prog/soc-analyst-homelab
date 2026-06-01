# Lab 5 — Splunk SPL Queries & Log Analysis

## Objective
Ingest Wazuh alerts into Splunk and use SPL to search,
filter, and visualize security events.

## Environment
- SIEM: Splunk Enterprise 9.2.1
- Data Source: Wazuh alerts.log
- Host: SOC-SIEM (192.168.56.9:8000)

## Setup
1. Installed Splunk on SOC-SIEM Ubuntu VM
2. Added data source via Monitor → Files & Directories
3. Path: /var/ossec/logs/alerts/alerts.log
4. Sourcetype: syslog
5. Result: 350 events ingested

## SPL Queries Used

### Basic Search
