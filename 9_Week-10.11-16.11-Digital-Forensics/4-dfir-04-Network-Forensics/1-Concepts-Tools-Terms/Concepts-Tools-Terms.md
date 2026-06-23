# Network Forensics

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how packet captures, flow data, and protocol evidence help investigators reconstruct what happened across systems and time.

### 2. Key ideas
- Network forensics examines communications rather than only host artifacts.
- Useful evidence can come from packets, flows, DNS records, proxy logs, IDS alerts, and protocol metadata.
- Encryption limits content visibility, but timing, endpoints, certificate metadata, and traffic patterns can still be valuable.
- Strong investigations combine network evidence with endpoint, authentication, and timeline data.

### 3. Tools and practical relevance
- Wireshark helps inspect PCAP data in detail.
- Zeek and similar tools help summarize protocol behavior at scale.

### 4. Key takeaway
Network forensics is often the best way to connect events across multiple systems, even when host visibility is incomplete.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Wireshark | Inspect captured traffic in detail |
| Zeek | Produce structured protocol telemetry from traffic |
| Flow collection tools | Summarize network conversations at scale |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| PCAP | Raw packet capture file |
| Flow record | Summary of a network conversation |
| Session reconstruction | Rebuilding a communication sequence from captured data |
| DNS evidence | Domain lookup traces that reveal intent or destinations |
| Protocol analysis | Reviewing traffic structure and meaning |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| capture | collect traffic for review |
| stream | sequence of related packets |
| endpoint | host or service involved in communication |
| metadata | descriptive data about traffic |
| reconstruct | rebuild events from evidence |
