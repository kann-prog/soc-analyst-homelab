# Module 3 — Alert Triage & Incident Investigation

## Triage Workflow
1. Alert fires
2. Identify alert type (Threat / Compliance / Integrity)
3. Read raw event data
4. Ask 3 triage questions
5. Assign verdict
6. Document in ticket
7. Escalate or close

## 3 Triage Questions
1. Is this a user mistake or an attacker?
2. Did it succeed after the failures?
3. Where did it come from?

## Verdict Types
- True Positive (TP): Real attack — escalate to L2
- False Positive (FP): Confirmed safe — close ticket
- Benign True Positive (BTP): Authorized activity — close
- False Negative (FN): Attack missed — most dangerous

## Escalate to L2 When
- Failed logins followed by success on same account
- External IP targeting Admin account
- Alert level 12 or above
- Same pattern across multiple machines
- Malware hash detected

## Attack Patterns
- Brute Force: Multiple 4625, same account, fast — T1110
- Password Spray: Multiple 4625, different accounts, slow — T1110.003
- Compromise: 4625 then 4624 same account — T1078
- Lateral Movement: 4648 across internal machines — T1021
- Persistence: 4720 or 4698 after suspicious login — T1136

## L1 vs L2
- L1: Triage, document, escalate, follow playbooks
- L2: Investigate, forensics, containment, write playbooks
