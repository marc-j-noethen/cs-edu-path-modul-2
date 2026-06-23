# change names of files into one you exported from Event Viever

**Course:** Cyber Security Analyst - Security Monitoring & SIEM | **Date:** 03 November 2025

---

## Task

**Goal:**  
Correlate events from your ingested Windows Security logs to detect a sequence of potentially malicious actions: a new service installation followed by a suspicious process creation from the same host. This is a challenging exercise that requires combining multiple events.

**Requirements:**

- Ensure your Windows VM is running and you have PowerShell open as Administrator.
    
- Activate auditing policy on your Windows 11:
    
- **Simulate Events:**
    
- Install a dummy service:
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```spl
index=Windows11 sourcetype=WinEventLog:Security (EventCode=4697 OR EventCode=4688)
| eval host_key=coalesce(host, ComputerName)
| transaction host_key maxspan=2m
| search EventCode=4697 EventCode=4688 (NewProcessName="*calc.exe" OR NewProcessName="*notepad.exe")
| table _time host_key ServiceName NewProcessName duration eventcount
```

- This correlates a service installation event with a follow-up process creation on the same host within 2 minutes.
- The screenshot should show the matching result set from Splunk.








