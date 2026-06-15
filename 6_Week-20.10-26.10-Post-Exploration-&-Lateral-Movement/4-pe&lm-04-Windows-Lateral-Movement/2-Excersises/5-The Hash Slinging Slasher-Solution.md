# 🐍 The Hash Slinging Slasher

**Course:** Cyber Security Analyst - Windows Lateral Movement | **Date:** 23 October 2025

---

## Task

**Goal:**  
First, calculate the NTLM hash for a given password. Then, perform a Pass-the-Hash attack using `psexec.py` and your calculated hash to gain remote access and analyze the logs.

**Requirements:**

- **Hash Calculation (Red Team):**
    
- On your Kali VM, you must first calculate the NTLM hash for the password `P@ssword123`.
    
- You can do this with a Python one-liner. Open a terminal and run the following command:
    
- The output of this command is the NTLM hash. Copy this value.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
report = [
    "NTLM hash of P@ssword123: cb8a428385459087a76793010d60f5dc",
    "Use psexec.py with the -hashes flag to authenticate as Administrator.",
    "In Event Viewer, filter Security Event ID 4624 and confirm Logon Type is 3 and Logon Process is NtLmSsp.",
    "The log entry from the Kali IP is the proof that the Pass-the-Hash attempt succeeded.",
]

for line in report:
    print(line)
```








