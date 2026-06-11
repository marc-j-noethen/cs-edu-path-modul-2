# Cross-Site Scripting (XSS)

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains cross-site scripting, the main XSS categories, their impact in the browser, and the core defenses used in modern web applications.

### 2. Key ideas
- XSS happens when untrusted data is included in a page without the right output encoding or sanitization.
- The browser executes the injected script in the context of the trusted site.
- The three main forms are reflected XSS, stored XSS, and DOM-based XSS.
- Output encoding, context-aware escaping, input handling, and content security policy all play defensive roles.

### 3. Tools and practical relevance
- Browser developer tools help confirm how input is rendered in the DOM.
- Intercepting proxies help identify which user inputs reach the page or the client-side code path.

### 4. Key takeaway
XSS is a browser trust problem: if untrusted input is treated like code, the browser will do exactly what the attacker wants.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Browser developer tools | Inspect rendered HTML, scripts, and DOM changes |
| Burp Suite | Trace how user input travels through requests and responses |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| XSS | Injection of untrusted script into a trusted web context |
| Reflected XSS | Malicious input is returned immediately in the response |
| Stored XSS | Malicious input is stored and later shown to users |
| DOM-based XSS | Vulnerability caused entirely by client-side code behavior |
| Content Security Policy | Browser policy that restricts script execution sources |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| render | display content in the browser |
| encode | transform special characters so they are treated as data |
| sanitize | remove or safely allow specific input |
| script | code executed in the browser |
| origin | security boundary for a web application in the browser |
