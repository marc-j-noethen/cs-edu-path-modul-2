# Attacking Active Directory

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains why Active Directory is a high-value target and how privilege relationships, delegation, and identity design can create attack paths.

### 2. Key ideas
- Active Directory attacks often exploit trust relationships more than software bugs.
- Excessive privileges, weak delegation, risky service account design, and stale administration paths all increase exposure.
- Attack paths in AD are usually chains of permissions and access rather than one isolated weakness.
- Defensive priorities include tiered administration, strong credential hygiene, privileged access review, and continuous visibility into identity relationships.

### 3. Tools and practical relevance
- Directory mapping and graph-based analysis tools help defenders understand privilege pathways in complex environments.
- Administrative review and identity governance are as important as technical hardening.

### 4. Key takeaway
In Active Directory, small trust mistakes can become major attack paths. Identity design is security design.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Directory analysis tools | Visualize privilege relationships and trust paths |
| Identity governance processes | Review rights, roles, and exceptions over time |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Delegation | Allowing one service or system to act on behalf of another identity |
| Service account | Account used by an application or service |
| Privileged group | Group with elevated administrative rights |
| Trust relationship | Security relationship between identities, systems, or domains |
| Attack path | Sequence of reachable steps leading to higher privilege or wider access |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| privilege | elevated access right |
| relationship | connection that affects trust or access |
| delegate | authorize one entity to act for another |
| stale | outdated but still present |
| governance | structured oversight of security-relevant decisions |
