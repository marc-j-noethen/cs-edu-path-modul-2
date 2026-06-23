# 🐍 The Celebrity Hunt

**Course:** Cyber Security Analyst - Network Security Monitoring | **Date:** 05 November 2025

---

## Task

**Goal:**  
Perform a miniature threat hunt. Given a packet capture of an attack that was missed by existing tools, you must manually identify the malicious activity, find the malware that was downloaded, and write a new IDS signature to detect the threat in the future.

**Requirements:**

- Go to [Malware-Traffic-Analysis.net](https://www.malware-traffic-analysis.net/) and download the PCAP for the "2020-09-08 - TRAFFIC ANALYSIS EXERCISE - URSNIF (GOZI) INFECTION WITH COBALT STRIKE" exercise: [https://www.malware-traffic-analysis.net/2023/07/12/index.html](https://www.malware-traffic-analysis.net/2023/07/12/index.html)
    
- Using the skills you've learned, analyze this PCAP with Zeek. Your first goal is to find the initial malware download, which happens over unencrypted HTTP. Look through the `http.log` and `files.log` to identify the downloaded executable (`.exe`) file.
    
- Once you've identified the file transfer in the logs, use Wireshark to find that same HTTP stream in the PCAP and export/carve the malicious executable file to your machine. (Warning: Do this in a safe environment; do not run the file).
    
- Now that you have the file, your job is to write a Snort rule to detect its transfer. Your rule must be specific enough to detect this malware but not so specific that it's trivial for an attacker to change. A good rule might look for a unique combination of the HTTP request headers (like the `User-Agent` and `Host`) and a unique byte sequence or string from the file's content itself.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```text
# Inputs
context = 'Local analysis or lab environment'
objective = 'Perform a miniature threat hunt. Given a packet capture of an attack that was missed by existing tools, you must manually identify the malicious activity, find the malware that was downloaded, and write a new IDS signature to detect the threat in the future.'
evidence = 'The custom Snort rule you wrote.'

# Main logic
1. Read the exercise carefully and split it into the required sub-tasks.
2. Match each sub-task to the correct security concept, control, or action.
3. Validate the final result against the stated goal before submission.
4. Present the answer in the exact format requested by the task.
```

**Alternative (compact):**

```text
I answered the required sub-tasks for "The Celebrity Hunt" and submitted the requested format.
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








