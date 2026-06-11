# Phishing Attacks and Email Defenses

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic covers how phishing emails work, how to recognize common warning signs, and how technical email defenses help reduce risk.

### 2. Key ideas
- Phishing works by making fraudulent communication look trustworthy enough to trigger a click, reply, or login.
- Common signs include urgency, mismatched links, unusual sender domains, unexpected attachments, and requests for secrets.
- Email headers and DNS-based controls help defenders evaluate whether a message is legitimate.
- SPF, DKIM, and DMARC improve email authentication, but user awareness is still necessary.

### 3. Tools and practical relevance
- DNS lookup tools help inspect SPF, DKIM, and DMARC-related records.
- Header analysis tools help analysts review sender paths and authentication results.

### 4. Key takeaway
Phishing is a mix of social engineering and technical deception, so defense needs both user judgment and technical controls.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| DNS lookup tools | Review email-related DNS records |
| Email header analyzer | Inspect sender path and authentication metadata |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Phishing | Fraudulent message intended to steal data or trigger action |
| Spear phishing | Highly targeted phishing aimed at a specific person or group |
| SPF | DNS-based policy that declares which servers may send mail for a domain |
| DKIM | Cryptographic email signing to support integrity and authenticity checks |
| DMARC | Policy and reporting layer built on SPF and DKIM |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| sender | claimed source of the email |
| domain | internet name associated with a service or organization |
| attachment | file included with an email |
| link | URL embedded in a message |
| spoofing | pretending to be someone or something else |
