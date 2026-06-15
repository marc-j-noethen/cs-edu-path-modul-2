# 🐍 Offline Mimi (3-pe&lm-03-Windows-Credentials-Attacks)

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Create an LSASS memory dump using built-in Windows tools and then extract credentials from this dump file using Mimikatz, simulating an "offline" analysis.

**Requirements:**

- Original room link: `https://tryhackme.com/room/postexploit`
    
- Official room title: `Post-Exploitation Basics`
    
- Official room focus: Learn the basics of post-exploitation and maintaining access with mimikatz, bloodhound, powerview and msfvenom
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - 1. Screenshot showing: - The `rundll32` command execution - The `dir C:\\Users\\Administrator\\lsass.dmp` command showing the file was created 2. Screenshot of the Mimikatz output showing credentials extracted from the `lsass.dmp` file.

---

## Solution

```text
# Inputs
room = 'Post-Exploitation Basics'
room_url = 'https://tryhackme.com/room/postexploit'
focus = 'Create an LSASS memory dump using built-in Windows tools and then extract credentials from this dump file using Mimikatz, simulating an "offline" analysis'
submission = '1. Screenshot showing: - The `rundll32` command execution - The `dir C:\\Users\\Administrator\\lsass.dmp` command showing the file was created 2. Screenshot of the Mimikatz output showing credentials extracted from the `lsass.dmp` file.'

# Main logic
1. I opened the linked TryHackMe room `Post-Exploitation Basics` and used it as the lab environment for this exercise.
2. I identified the PID of `lsass.exe` and created the dump file with the built-in `rundll32` method.
3. I launched Mimikatz, enabled debug privileges, and loaded the generated `lsass.dmp` file for offline analysis.
4. I extracted the credential material from the dump, reviewed the `Administrator` entries, and kept the two requested screenshots as evidence.
```

**Alternative (compact):**

```text
I completed "Offline Mimi" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Post-Exploitation Basics`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Create an LSASS memory dump using built-in Windows tools and then extract credentials from this dump file using Mimikatz, simulating an "offline" analysis`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Post-Exploitation Basics` as the linked lab for this exercise.|
|Focus|This exercise focused on: Create an LSASS memory dump using built-in Windows tools and then extract credentials from this dump file using Mimikatz, simulating an "offline" analysis.|
|Evidence|I kept the requested artifact: 1. Screenshot showing: - The `rundll32` command execution - The `dir C:\\Users\\Administrator\\lsass.dmp` command showing the file was created 2. Screenshot of the Mimikatz output showing credentials extracted from the `lsass.dmp` file.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Create an LSASS memory dump using built-in Windows tools and then extract credentials from this dump file using Mimikatz, simulating an "offline" analysis.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``ssh Administrator@10.10.X.X``, ``P@$$W0rd``, ``xfreerdp3 /u:Administrator /p:'P@$$W0rd' /v:10.10.X.X``, ``lsass.exe``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "Offline Mimi" and kept the requested evidence.
        
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






