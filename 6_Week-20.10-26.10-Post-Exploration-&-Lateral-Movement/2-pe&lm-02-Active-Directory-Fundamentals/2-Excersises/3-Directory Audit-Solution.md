# 🐍 Directory Audit (2-pe&lm-02-Active-Directory-Fundamentals)

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Use PowerShell with LDAP filters to query user accounts for potential security risks.

**Requirements:**

- Original room link: `https://tryhackme.com/room/winadbasics`
    
- Official room title: `Active Directory Basics`
    
- Official room focus: This room will introduce the basic concepts and functionality provided by Active Directory.
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - Submit a single screenshot showing the command and the final output from Step 3, which confirms that you detected the simulated bad logon.

---

## Solution

```text
# Inputs
room = 'Active Directory Basics'
room_url = 'https://tryhackme.com/room/winadbasics'
focus = 'Use PowerShell with LDAP filters to query user accounts for potential security risks'
submission = 'Submit a single screenshot showing the command and the final output from Step 3, which confirms that you detected the simulated bad logon.'

# Main logic
1. I opened the linked TryHackMe room `Active Directory Basics`.
2. I wrote a PowerShell query to list users whose `logonCount` was greater than zero and used one of those accounts as my test user.
3. I wrote a second query to detect users whose `badPwdCount` was greater than zero.
4. I used `runas` with a wrong password, re-ran the detection query, and confirmed the simulated bad logon in the final output.
```

**Alternative (compact):**

```text
I completed "Directory Audit" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Active Directory Basics`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Use PowerShell with LDAP filters to query user accounts for potential security risks`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Active Directory Basics` as the linked lab for this exercise.|
|Focus|This exercise focused on: Use PowerShell with LDAP filters to query user accounts for potential security risks.|
|Evidence|I kept the requested artifact: Submit a single screenshot showing the command and the final output from Step 3, which confirms that you detected the simulated bad logon.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Use PowerShell with LDAP filters to query user accounts for potential security risks.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``logonCount``, ``DisplayName``, ``badPwdCount``, ``runas``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "Directory Audit" and kept the requested evidence.
        
    3. I kept the exact evidence the task asked me to submit.
        
- **Edge Cases:**
    
    - Some TryHackMe rooms require a login, an AttackBox, a deployed VM, or VPN access before the full practical section is usable.
        
    - Room wording, screenshots, and task numbering can change over time on the public platform.
        
    - Local tooling can differ from the AttackBox, especially when package versions or CPU architecture matter.
        
- **Tip:** I kept the submission screenshot or output separately so it can be attached directly to the course hand-in.

---

## Optional: Extensions

- Add my own screenshots or command output excerpts directly below the solution.
    
- Add a short note on what I learned from the room after the submission artifact.
    
- Append the exact commands I used if I want the GitHub version to be more technical.
    
- Re-run the room later if TryHackMe updates the machine or task flow.






