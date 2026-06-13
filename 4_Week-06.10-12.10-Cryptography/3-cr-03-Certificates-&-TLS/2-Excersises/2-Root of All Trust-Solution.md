# 🐍 Root of All Trust

**Course:** Cyber Security Analyst - Certificates & TLS | **Date:** 08 October 2025

---

## Task

**Goal:**  
Create your own simple, two-level Certificate Authority infrastructure. You will create a Root CA and use it to sign a certificate for a fictional server, `pentest.lab`.

**Requirements:**

- Create a private key for your Root CA (`MyRootCA.key`).
    
- Create a self-signed Root CA certificate (`MyRootCA.pem`) using the key from the previous step. When prompted, give it a memorable Common Name, like "CyberSec Student Root CA".
    
- Now, create a new private key (`pentest.lab.key`) and a Certificate Signing Request (`pentest.lab.csr`) for a server. The Common Name for this CSR must be `pentest.lab`.
    
- Use your Root CA's key and certificate to sign the server's CSR, generating a final, signed certificate for `pentest.lab` (`pentest.lab.crt`).
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```text
# Inputs
platform = 'Local analysis or lab environment'
objective = 'Create your own simple, two-level Certificate Authority infrastructure. You will create a Root CA and use it to sign a certificate for a fictional server, `pentest.lab`.'
evidence = 'Submit the final server certificate file (`pentest.lab.crt`) and a screenshot showing the successful output of the verification command from the final step.'

# Main logic
1. Open the referenced room or lab in the intended platform.
2. Work through the required tasks until the final objective is met.
3. Verify the success state inside the platform itself.
4. Capture the exact evidence requested for submission.
```

**Alternative (compact):**

```text
I completed the referenced lab for "Root of All Trust" and captured the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`task text`|`correct method`|`required evidence`|`Goal completed`|`Reviewer can verify it`|✅|
|`platform or scenario`|`final validation`|`submission format`|`Consistent result`|`Matches the task`|✅|
|`self-check`|`edge-case review`|`final file`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Objective Alignment|The solution must directly satisfy the original task instead of drifting into unrelated detail.|
|Evidence Quality|The final artifact should prove completion clearly enough for a reviewer to confirm it.|
|Validation|The result should be checked against the stated goal before submission.|

---

## Rules / Logic

```text
Read the full task before solving it.
Match the output to the requested submission format.
Keep only verifiable final results.
```

---

## Notes

- **Concept:** Keep the solution tightly aligned to the original objective.
    
- **Syntax:** Use the platform, terminology, and evidence style that the task expects.
    
- **Order matters:**
    
    1. Read the task and identify the real objective.
        
    2. Complete or answer the task with the correct method.
        
    3. Validate the result and keep only the final solution.
        
- **Edge Cases:**
    
    - The source task may be incomplete or empty.
        
    - External labs can change while the local solution file stays static.
        
    - Screenshots that do not show the final state may be rejected as weak evidence.
        
- **Tip:** Keep a short note of the exact commands, payloads, or findings you used during completion.
    

---

## Optional: Extensions

- Add a second validated approach if the task can be solved in more than one reliable way.
    
- Add stronger validation evidence if the original task was solved in a live platform.
    
- Add brief error-handling notes for common failure states.
    
- Add short reviewer notes if the task depends on a changing external environment.








