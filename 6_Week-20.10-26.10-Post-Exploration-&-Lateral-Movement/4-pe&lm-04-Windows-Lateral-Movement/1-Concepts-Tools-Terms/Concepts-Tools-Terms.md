# Windows Lateral Movement

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains lateral movement: how access expands from one compromised Windows system to other systems in the same environment.

### 2. Key ideas
- Lateral movement depends on both access and trust, not only on technical exploits.
- Common pathways involve remote administration protocols, reused credentials, excessive privileges, and weak segmentation.
- In enterprise incidents, lateral movement often matters more than the original entry point because it increases blast radius.
- Detection depends on seeing unusual remote logons, service creation, admin tool use, and cross-host process chains.

### 3. Tools and practical relevance
- Windows logs, Sysmon-style telemetry, and EDR data help trace remote execution and privilege use.
- Network segmentation and privileged-access controls reduce lateral movement opportunities.

### 4. Key takeaway
An attacker who can move laterally can turn a local problem into an enterprise-wide incident.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Windows Event Logs | Track logons, service activity, and remote execution traces |
| EDR | Connect events across endpoints |
| Firewall and segmentation controls | Limit reachable pathways between systems |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Lateral movement | Moving from one system to another after initial compromise |
| WinRM | Windows Remote Management protocol |
| RDP | Remote Desktop Protocol for interactive remote access |
| WMI | Windows Management Instrumentation used for administration and visibility |
| Segmentation | Restricting communication paths between systems or zones |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| pivot | use one system as a stepping stone to another |
| remote | performed across a network |
| logon | authentication event to a system or service |
| blast radius | extent of impact after compromise |
| pathway | possible route for access or movement |
