# Active Reconnaissance

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic covers active reconnaissance: directly interacting with a target system or network to discover live hosts, open ports, and running services.

### 2. Key ideas
- Active recon sends traffic to the target, so it is more visible than passive recon.
- Common goals are host discovery, port identification, service detection, and basic fingerprinting.
- Good testers balance thoroughness with scope, rate limits, and the risk of disruption.
- Active recon should only be performed in approved environments because it can trigger alerts or affect fragile systems.

### 3. Tools and practical relevance
- Nmap is widely used for host discovery, port scanning, and service detection.
- Ping and traceroute help understand reachability and network path behavior.
- Curl can be used for basic manual checks of HTTP and HTTPS services.

### 4. Key takeaway
Active reconnaissance turns guesses into evidence, but it must be controlled, scoped, and authorized.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Nmap | Discover hosts, open ports, and service details |
| ping | Test basic reachability |
| traceroute | Observe the path to a remote system |
| curl | Check web responses and headers manually |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Active reconnaissance | Direct probing of a target to gather technical data |
| Host discovery | Determining which systems are alive |
| Port scanning | Checking which network ports are open |
| Banner grabbing | Collecting identifying information from a service response |
| Service detection | Identifying the protocol or software behind an open port |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| probe | network request used to test a target |
| response | answer returned by the target |
| open port | reachable service endpoint on a host |
| fingerprint | identifying characteristics of a system or service |
| scope | approved testing boundary |
