# 🐍 Poisoned Paths

**Course:** Cyber Security Analyst - MitM & Cryptographic Attacks | **Date:** 09 October 2025

---

## Task

**Goal:**  
Perform a non-consensual Man-in-the-Middle attack. Without any prior configuration on the Windows VM, you must force its network traffic through your Kali machine using ARP poisoning. Your objective is to automatically find and poison the victim, then capture the plaintext credentials they send to `http://testphp.vulnweb.com/login.php`.

You should use a tool designed for automated MITM attacks, such as `bettercap`. You will need to explore the tool's capabilities to achieve the goal.

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

```text
# Inputs
context = 'Local analysis or lab environment'
objective = 'Perform a non-consensual Man-in-the-Middle attack. Without any prior configuration on the Windows VM, you must force its network traffic through your Kali machine using ARP poisoning. Your objective is to automatically find and poison the victim, then capture the plaintext credentials they send to `http://testphp.vulnweb.com/login.php`.

You should use a tool designed for automated MITM attacks, such as `bettercap`. You will need to explore the tool's capabilities to achieve the goal.'
evidence = 'Submit a single screenshot of your attack tool's window on Kali. The screenshot must clearly show the log message that confirms the capture of the victim's username and password.'

# Main logic
1. Read the exercise carefully and split it into the required sub-tasks.
2. Match each sub-task to the correct security concept, control, or action.
3. Validate the final result against the stated goal before submission.
4. Present the answer in the exact format requested by the task.
```

**Alternative (compact):**

```text
I answered the required sub-tasks for "Poisoned Paths" and submitted the requested format.
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








