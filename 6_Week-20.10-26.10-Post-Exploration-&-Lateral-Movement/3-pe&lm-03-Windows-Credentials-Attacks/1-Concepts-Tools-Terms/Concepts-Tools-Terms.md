# Windows Credential Attacks

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains why credential material in Windows environments is so valuable and how different credential-abuse patterns create enterprise risk.

### 2. Key ideas
- Attackers do not always need plaintext passwords; hashes, Kerberos tickets, and cached secrets can also be abused.
- Credential attacks often focus on collection, replay, cracking, or misuse of existing trust.
- Enterprise impact is high because one compromised credential can unlock many systems.
- Defensive priorities include MFA, credential isolation, privileged access hygiene, rapid revocation, and strong endpoint visibility.

### 3. Tools and practical relevance
- Credential Guard and modern endpoint protections help reduce access to sensitive credential material.
- Centralized logging helps defenders detect unusual authentication patterns and account behavior.

### 4. Key takeaway
Credentials are not just passwords. In Windows environments, many different authentication artifacts must be protected.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Credential Guard | Help isolate sensitive credential material on supported Windows systems |
| EDR and log platforms | Detect suspicious authentication and endpoint behavior |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| NTLM hash | Password-derived value used in legacy Windows authentication flows |
| Kerberos ticket | Time-limited authentication artifact in Kerberos environments |
| Credential dumping | Attempt to extract credential material from a system |
| Password spraying | Trying a small number of passwords against many accounts |
| Replay | Reusing valid authentication material without knowing the original secret |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| hash | derived authentication value |
| ticket | credential-like proof used in Kerberos |
| cache | stored data used again later |
| revoke | invalidate a credential or access path |
| rotate | replace a secret with a new one |
