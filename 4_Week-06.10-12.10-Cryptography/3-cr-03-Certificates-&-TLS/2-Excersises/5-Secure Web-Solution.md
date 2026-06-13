# 🐍 Secure Web

**Course:** Cyber Security Analyst - Certificates & TLS | **Date:** 08 October 2025

---

## Task

**Goal:**  
The objective of this exercise is to secure a local web application with a valid SSL certificate from a trusted Certificate Authority (CA), Let's Encrypt. You will configure a simple web app, obtain a certificate using `certbot`, and confirm the secure connection in your browser by seeing the trusted padlock icon.

**Requirements:**

- Read the task carefully and identify the exact objective.
    
- Apply the correct concept, method, or platform workflow.
    
- Validate the final result against the stated goal.
    
- Submit only the evidence or answer format requested.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
report = [
    "Use certbot with a DNS-01 challenge for the deSEC domain.",
    "Configure the Flask app to serve fullchain.pem and privkey.pem over HTTPS.",
    "Map the real domain to 127.0.0.1 in /etc/hosts for local testing.",
    "Open the domain in the browser and confirm the trusted padlock is shown.",
]

for line in report:
    print(line)
```








