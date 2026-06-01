# Lab 2 — Network Packet Analysis with Wireshark

## Objective
Capture and analyze network traffic to identify attack
patterns at the packet level.

## Environment
- Analyst Machine: Kali Linux (192.168.56.8)
- Target: Metasploitable2 (192.168.56.11)
- Tool: Wireshark 4.4.6

## Steps Performed

### 1. Basic Traffic Capture
Captured ICMP traffic while pinging google.com.
Identified TTL values for OS fingerprinting.

| TTL | OS |
|---|---|
| 64 | Linux / Unix |
| 128 | Windows |
| 255 | Cisco / Network device |

### 2. Wireshark Filters Used
| Filter | Purpose |
|---|---|
| icmp | Show only ping traffic |
| dns | Detect C2 beaconing |
| ip.src == 10.0.2.15 | Outbound traffic from machine |
| ip.dst == 10.0.2.15 | Inbound traffic to machine |
| tcp.flags.syn == 1 && tcp.flags.ack == 0 | Detect port scan |
| tcp.port == 6200 | Detect backdoor shell |

### 3. Port Scan Detection
Ran Nmap against Metasploitable2 while capturing
on Wireshark interface eth1.

Port scan signature observed:
- Same source IP: 192.168.56.8
- Different destination ports: incrementing
- SYN only, no ACK — half-open scan
- High speed — milliseconds apart

Filter used: tcp.flags.syn == 1 && tcp.flags.ack == 0

### 4. Attack Traffic Capture
Captured vsftpd backdoor exploit on port 6200.
TCP stream showed root shell commands in plain text.

Filter: ip.addr == 192.168.56.11 && tcp.port == 6200

Commands visible in TCP stream:
- whoami → root
- id → uid=0(root) gid=0(root)
- cat /etc/passwd → full user list

## Key Learning
- Unencrypted shells expose every command to analysts
- TTL mismatch = possible OS spoofing
- SYN-only packets = port scan signature
- DNS regular intervals = C2 beaconing pattern
- Follow TCP Stream reveals full session content

## MITRE Mapping
- T1046 — Network Service Scanning
- T1190 — Exploit Public Facing Application
- T1059 — Command Line Interface
