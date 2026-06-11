# Credentials, Sessions, and Tokens

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains what attackers are often trying to steal in web environments: credentials, session identifiers, and tokens.

### 2. Key ideas
- HTTP is stateless, so applications need mechanisms to remember authenticated users.
- Sending credentials on every request is insecure and inefficient.
- Stateful sessions usually rely on a server-side session and a client-side session identifier, often in a cookie.
- Tokens are common in API-driven systems, but they are bearer secrets and must be protected just like passwords.

### 3. Tools and practical relevance
- This topic is mostly conceptual.
- Browser developer tools are useful for understanding cookies, headers, and storage behavior during training.

### 4. Key takeaway
If an attacker steals a valid session cookie or token, they may not need the user's password at all.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Browser developer tools | Inspect cookies, headers, and client-side storage |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Stateless protocol | Protocol that does not remember previous requests |
| Session | Server-side record that tracks a logged-in user |
| Session cookie | Client-side identifier that points to a session |
| Token | Credential-like value used to prove authorization or identity |
| Bearer token | Token that grants access to whoever possesses it |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| login | authentication event |
| cookie | small piece of browser-stored data |
| expiry | point in time when a session or token becomes invalid |
| revoke | invalidate a session or token |
| hijack | take over a valid session |
