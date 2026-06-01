# Module 2 — Wazuh Rules & Decoders

## Key Concepts
- Log pipeline: Raw Log → Decoder → Rule Engine → Alert
- Decoder parses raw logs into named fields
- Rules match decoded fields against threat patterns
- Custom rules go in /var/ossec/etc/rules/local_rules.xml
- Rule IDs 100000-109999 reserved for custom rules

## Rule Anatomy
- id: unique rule number
- level: severity 0-15
- if_sid: parent rule dependency
- field name: which decoded field to check
- frequency + timeframe: pattern-based detection

## Frequency Rules
- Fire only when pattern repeats within timeframe
- Prevents alert fatigue from single events
- Example: 5 failed logins in 60 seconds = brute force

## Test Rules Without Restart
- Command: /var/ossec/bin/wazuh-logtest

## MITRE Mapping
- T1110 — Brute Force (frequency-based detection)
