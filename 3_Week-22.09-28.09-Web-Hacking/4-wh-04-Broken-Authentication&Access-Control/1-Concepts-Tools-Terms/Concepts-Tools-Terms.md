# Broken Authentication and Access Control

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic covers how applications identify users, manage sessions, authorize actions, and what goes wrong when these controls are implemented poorly.

### 2. Key ideas
- Authentication answers "Who are you?" and authorization answers "What are you allowed to do?"
- Sessions, cookies, and tokens are central to keeping users logged in across stateless HTTP requests.
- Common failures include weak login flows, poor password reset handling, missing server-side authorization checks, and insecure session management.
- Strong defenses combine MFA, secure session settings, least privilege, and explicit server-side access checks.

### 3. Tools and practical relevance
- Browser developer tools help inspect cookies and token handling during training.
- Intercepting proxies help testers review whether access decisions are enforced consistently on the server side.

### 4. Key takeaway
Many access-control failures happen because the application trusts the client too much or checks permissions too late.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Browser developer tools | Inspect cookies, tokens, and client-side session behavior |
| Burp Suite | Review and replay requests to verify access checks |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Authentication | Verifying the identity of a user or system |
| Authorization | Determining what an authenticated identity may do |
| Session fixation | Forcing a user to authenticate with an attacker-known session identifier |
| Access control | Rules that restrict access to resources or actions |
| Least privilege | Granting only the minimum permissions necessary |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| login | process of authenticating a user |
| permission | allowed action |
| role | collection of permissions |
| session | logged-in state tracked by the application |
| enforce | apply a rule consistently |
