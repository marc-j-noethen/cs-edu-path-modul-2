# 🐍 A Room with a View 

**Course:** Cyber Security Analyst - Windows Lateral Movement | **Date:** 23 October 2025

---

## Task

**Goal:**  
Practice lateral movement using RDP and then identify the specific logon event this action creates in the Windows logs.

**Requirements:**

- **Attack (Red Team):**
    
- From your Kali Linux VM, open a terminal.
    
- Connect to your Windows 11 VM using xfreerdp3:
    
- Replace `YourPassword` with your Administrator password and `WINDOWS_IP` with your Windows 11 VM IP address.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```text
# Inputs
context = 'NIST reference material'
objective = 'Practice lateral movement using RDP and then identify the specific logon event this action creates in the Windows logs.'
evidence = 'Submit a screenshot of the Event Viewer from your RDP session. The screenshot must show the details of the Event ID 4624, with the **Logon Type: 10** clearly visible.'

# Main logic
1. Read the exercise carefully and split it into the required sub-tasks.
2. Match each sub-task to the correct security concept, control, or action.
3. Validate the final result against the stated goal before submission.
4. Present the answer in the exact format requested by the task.
```

**Alternative (compact):**

```text
I answered the required sub-tasks for "A Room with a View" and submitted the requested format.
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








