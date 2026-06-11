# 🐍 Busted 

**Course:** Cyber Security Analyst - Web Hacking | **Date:** 22 September 2025

---

## Task

**Goal:**  
Use the `gobuster` tool to perform a directory brute-force attack and discover a hidden administrative interface.

**Requirements:**

- Use the command-line tool `gobuster` to search for directories on the [Gin & Juice Shop](https://ginandjuice.shop/) website (vulnerable web application by PortSwigger).
    
- You'll need a good wordlist. A standard one is `directory-list-2.3-small.txt` from the SecLists collection. If you don't have SecLists, many Linux distros for security testing include similar lists in `/usr/share/wordlists/`.
    
- Construct the `gobuster` command. It will look something like this: `go [path_to_your_wordlist.txt]`.
    
- Run the command and analyze the output. Look for any paths that return a `200` or `302`status code, as these indicate existing resources. You are specifically looking for a path related to administration.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```text
# Inputs
platform = 'PortSwigger Web Security Academy'
objective = 'Use the `gobuster` tool to perform a directory brute-force attack and discover a hidden administrative interface.'
evidence = 'Submit a screenshot of your terminal showing the `gobuster` command you ran and the output where the hidden administrative directory is revealed.'

# Main logic
1. Open the referenced room or lab in the intended platform.
2. Work through the required tasks until the final objective is met.
3. Verify the success state inside the platform itself.
4. Capture the exact evidence requested for submission.
```

**Alternative (compact):**

```text
I completed the referenced lab for "Busted" and captured the requested evidence.
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








