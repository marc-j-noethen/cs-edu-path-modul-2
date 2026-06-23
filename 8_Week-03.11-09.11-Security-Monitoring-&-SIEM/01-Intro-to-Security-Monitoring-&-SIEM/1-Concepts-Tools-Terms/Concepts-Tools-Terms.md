# Introduction to Security Monitoring and SIEM

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic introduces security monitoring, log analysis, and the role of a SIEM in centralizing and correlating telemetry.

### 2. Key ideas
- Security monitoring is about turning raw telemetry into actionable visibility.
- A SIEM collects, normalizes, stores, searches, and correlates data from many sources.
- Alerts are only useful when they are tied to meaningful detection logic and investigation context.
- Good monitoring depends on log quality, time synchronization, retention, and clear ownership.

### 3. Tools and practical relevance
- SIEM platforms support centralized search, dashboards, and alerting.
- Log shippers and normalizers help bring data from many systems into a consistent format.

### 4. Key takeaway
Monitoring is not just collecting logs. It is building reliable visibility that helps people make decisions during suspicious events.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| SIEM platform | Centralize, correlate, and search security telemetry |
| Log shipper | Forward logs from systems to collection points |
| Normalization pipeline | Convert diverse log formats into consistent fields |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Telemetry | Technical observations collected from systems and networks |
| SIEM | Security information and event management platform |
| Correlation | Linking events together to reveal a larger pattern |
| Detection rule | Logic used to identify potentially important events |
| Retention | How long logs are stored |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| alert | signal that something may need attention |
| dashboard | visual summary of monitored data |
| ingest | bring data into a system |
| normalize | standardize data structure |
| search | query stored data efficiently |
