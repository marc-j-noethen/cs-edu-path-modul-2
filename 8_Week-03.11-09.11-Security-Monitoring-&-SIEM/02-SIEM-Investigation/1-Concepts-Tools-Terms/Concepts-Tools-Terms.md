# SIEM Investigation

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how analysts investigate SIEM alerts by pivoting across hosts, users, timestamps, and related telemetry.

### 2. Key ideas
- Investigation starts with triage: decide whether an alert is benign, suspicious, or clearly malicious.
- Analysts pivot from one clue to related data such as user, host, IP, process, or time window.
- Good investigations test hypotheses instead of collecting random facts.
- Context from baselines, asset criticality, and threat intelligence helps avoid both underreaction and overreaction.

### 3. Tools and practical relevance
- SIEM search and pivot features are central to investigation work.
- Case-management workflows help document evidence, decisions, and escalation steps.

### 4. Key takeaway
The goal of an investigation is not to collect more data forever. It is to reach a defensible conclusion quickly and clearly.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| SIEM search interface | Pivot through related telemetry efficiently |
| Case management workflow | Track evidence, ownership, and response decisions |
| Threat intelligence enrichment | Add context to indicators and entities |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Triage | Initial assessment of urgency and credibility |
| Pivot | Use one data point to find related evidence |
| Baseline | Expected normal behavior used for comparison |
| False positive | Alert that appears suspicious but is not malicious |
| Escalation | Passing a case to a higher level of response or expertise |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| entity | user, host, IP, process, or other tracked object |
| timeline | ordered sequence of events |
| evidence | data that supports a conclusion |
| scope | extent of affected systems or activity |
| conclude | decide based on available facts |
