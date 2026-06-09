# Passive Reconnaissance

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic covers passive reconnaissance: gathering information about a target without directly interacting with its systems.

### 2. Key ideas
- Passive reconnaissance relies on public or third-party sources rather than direct probing of the target.
- The goal is to build a target profile: domains, subdomains, technology stack, public infrastructure, contacts, and business context.
- Good passive recon reduces noise, lowers detection risk, and makes later testing more focused.
- OSINT is valuable, but information still needs validation because public data can be stale or incomplete.

### 3. Tools and practical relevance
- WHOIS helps identify domain registration details and sometimes useful infrastructure clues.
- DNS lookups reveal records such as A, MX, NS, and TXT entries.
- Shodan and search engines help identify exposed services, technology fingerprints, and public references.

### 4. Key takeaway
Passive recon is about learning as much as possible before touching the target directly.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| WHOIS | Query domain registration and ownership information |
| DNS lookup tools | Review DNS records and naming structure |
| Shodan | Search for publicly exposed internet services |
| Search engines | Collect open-source intelligence and public references |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Reconnaissance | Information gathering about a target |
| OSINT | Open-source intelligence from public sources |
| Passive reconnaissance | Recon performed without direct target interaction |
| DNS | Domain Name System used for name resolution |
| Certificate transparency | Public logging of issued TLS certificates |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| target profile | structured picture of the target environment |
| subdomain | domain below a parent domain |
| metadata | supporting information about data or systems |
| footprint | observable external presence of a target |
| exposure | information or service visible from the outside |
