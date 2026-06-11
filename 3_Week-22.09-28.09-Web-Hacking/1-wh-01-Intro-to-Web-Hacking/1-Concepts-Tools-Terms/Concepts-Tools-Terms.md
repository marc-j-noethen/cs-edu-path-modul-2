# Introduction to Web Hacking

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic introduces the web application attack surface, the basic tester workflow, and the role of an intercepting proxy.

### 2. Key ideas
- Web applications are built on HTTP, HTML, CSS, JavaScript, cookies, and back-end logic.
- A security tester focuses on real requests and responses, not only on what the browser interface allows.
- Intercepting, inspecting, and modifying traffic is central to understanding web behavior.
- Good web testing starts with mapping functionality, trust boundaries, inputs, and authentication flows.

### 3. Tools and practical relevance
- Browser developer tools show requests, responses, cookies, storage, and client-side code behavior.
- Burp Suite is a standard intercepting proxy for authorized web testing.
- Repeater helps retest individual requests in a controlled way.

### 4. Key takeaway
Web security work becomes much clearer once you stop thinking in pages and start thinking in HTTP transactions.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Browser developer tools | Inspect requests, responses, cookies, and front-end behavior |
| Burp Suite | Intercepting proxy for authorized web testing |
| Burp Repeater | Manually resend and modify a single HTTP request |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| HTTP | Protocol used by browsers and web servers |
| Cookie | Small piece of state stored by the browser |
| Parameter | User-controllable value included in a request |
| Intercepting proxy | Tool that sits between client and server traffic |
| Attack surface | Reachable parts of an application that can be tested or abused |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| request | message sent from client to server |
| response | message returned from server to client |
| header | metadata in a request or response |
| body | main content of a request or response |
| workflow | repeatable sequence of testing steps |
