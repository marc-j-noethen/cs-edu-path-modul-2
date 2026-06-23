# Endpoint Security Monitoring

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how to monitor endpoints such as workstations and servers for suspicious execution, persistence, and user activity.

### 2. Key ideas
- Endpoint monitoring provides detail that network monitoring alone cannot show, such as process lineage, command lines, file changes, and local persistence.
- Useful endpoint visibility often comes from operating-system logs, Sysmon-style telemetry, and EDR data.
- Individual endpoint events can look harmless, so context and correlation are essential.
- Detection quality improves when defenders understand normal administrative behavior and common attacker tradecraft.

### 3. Tools and practical relevance
- Sysmon-style telemetry gives richer process and file visibility than default logs alone.
- EDR platforms help analysts investigate suspicious endpoint chains quickly.

### 4. Key takeaway
Endpoints are where many attacks become visible in full detail. Strong endpoint telemetry is one of the most valuable defensive assets.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Windows Event Logs | Record system, authentication, and application activity |
| Sysmon | Expand endpoint telemetry for detection and hunting |
| EDR | Correlate and investigate endpoint events |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Endpoint | User or server system at the edge of the network |
| Process lineage | Parent-child view of process execution |
| Persistence | Mechanism used to survive reboot or re-entry |
| Living off the land | Abuse of legitimate built-in tools for malicious goals |
| Telemetry | Recorded technical evidence about system behavior |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| process | running program instance |
| command line | arguments used to start a process |
| parent | process that launched another process |
| artifact | observable trace on a system |
| hunt | proactively search for suspicious patterns |
