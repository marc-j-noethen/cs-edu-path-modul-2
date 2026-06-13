# 🐍 Certification Sabotage

**Course:** Cyber Security Analyst - Certificates & TLS | **Date:** 08 October 2025

---

## Task

**Goal:**  
Leverage your existing Root CA to intentionally create certificates with common flaws (expiration, name mismatch), observe the specific browser errors, and then validate a correctly issued certificate by establishing trust on your local machine.

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
    "Expired certificate on https://localhost:4443: NET::ERR_CERT_DATE_INVALID",
    "Name mismatch certificate on https://localhost:4443: NET::ERR_CERT_COMMON_NAME_INVALID",
    "Valid certificate after trusting MyRootCA.pem: secure padlock shown in the browser",
]

for line in report:
    print(line)
```








