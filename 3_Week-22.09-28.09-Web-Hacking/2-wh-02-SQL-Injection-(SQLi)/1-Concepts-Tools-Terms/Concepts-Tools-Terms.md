# SQL Injection

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains SQL injection: how unsafe input handling can alter database queries and why parameterized queries are the main defense.

### 2. Key ideas
- SQL injection happens when untrusted input is mixed into database queries in an unsafe way.
- The impact can include data disclosure, data modification, authentication bypass, or application instability.
- The root cause is not "special SQL magic" but broken separation between code and data.
- The most important defense is parameterized queries, supported by input validation, least privilege, and secure error handling.

### 3. Tools and practical relevance
- Intercepting proxies help developers and testers understand where user-controlled data enters the application.
- Application logs and secure coding reviews help confirm whether data reaches database queries safely.

### 4. Key takeaway
SQL injection is fundamentally a secure coding problem. If code and user input stay separate, the risk drops dramatically.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Burp Suite | Inspect where user input enters requests |
| Application logs | Help trace errors and unexpected database behavior |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| SQL injection | Unsafe query construction that lets input alter SQL behavior |
| Parameterized query | Query structure that keeps code separate from data |
| Input validation | Checking whether data is in an expected format |
| Least privilege | Giving the database account only the permissions it needs |
| ORM | Abstraction layer that can help reduce manual query risks when used correctly |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| query | database instruction |
| parameter | separately supplied input value |
| sanitize | clean or restrict input safely |
| disclosure | exposure of information |
| bypass | avoiding a security control |
