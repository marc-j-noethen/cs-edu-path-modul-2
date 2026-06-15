# Active Directory Fundamentals

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic introduces the main building blocks of Active Directory and why it is such a critical security boundary in Windows enterprise environments.

### 2. Key ideas
- Active Directory centralizes identity, authentication, authorization, and policy in many Windows environments.
- Core concepts include domains, domain controllers, users, groups, organizational units, group policy, and trusts.
- Kerberos and LDAP are fundamental protocols for identity and directory functions.
- AD security is not only about servers; it is about the trust relationships between people, systems, and privileges.

### 3. Tools and practical relevance
- Administrative consoles and directory tools help visualize users, groups, and policy structure.
- Understanding the logical model is essential for both defense and incident investigation.

### 4. Key takeaway
Active Directory is a trust system. Once that trust is weakly configured, compromise can spread far beyond a single machine.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Active Directory administrative tools | Review users, groups, and directory structure |
| Group Policy Management tools | Review and manage centralized policy |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Domain | Administrative and security boundary in AD |
| Domain controller | Server that authenticates users and stores directory data |
| Organizational unit | Container used to group objects and apply policy |
| Group Policy | Centralized configuration and security management mechanism |
| Trust | Relationship that allows authentication or access across boundaries |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| directory | structured store of identities and objects |
| principal | security identity such as a user or service |
| policy | centrally managed rule or configuration |
| group | collection of principals for permission management |
| forest | top-level AD structure that can contain one or more domains |
