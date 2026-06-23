# Network Security Monitoring

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how to monitor network activity for suspicious behavior using packet, flow, and protocol-level evidence.

### 2. Key ideas
- Network monitoring looks at communications between systems rather than only what happens on a single endpoint.
- Different data sources provide different value: packets, flows, DNS, HTTP metadata, TLS metadata, and IDS alerts.
- Visibility has limits because modern traffic is often encrypted, but metadata can still be extremely useful.
- Good monitoring depends on placement, retention, and knowing which protocols matter most to the environment.

### 3. Tools and practical relevance
- Wireshark helps inspect packets and protocol details.
- Zeek and Suricata-style tools help produce higher-level network telemetry and detections.

### 4. Key takeaway
You do not need to see every byte of plaintext to detect suspicious behavior. Metadata and patterns are often enough to surface real risk.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Wireshark | Inspect packet-level traffic |
| Zeek | Generate protocol-rich network telemetry |
| Suricata | Detect suspicious network activity and create alerts |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| PCAP | Packet capture data containing raw network traffic |
| NetFlow | Summarized record of network conversations |
| DNS telemetry | Visibility into domain name lookups |
| TLS metadata | Non-content information about encrypted sessions |
| IDS | Intrusion detection system for suspicious network activity |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| packet | smallest unit of transmitted network data |
| flow | summary of a network conversation |
| protocol | agreed communication format |
| sensor | place where traffic is observed |
| metadata | descriptive information about traffic |
