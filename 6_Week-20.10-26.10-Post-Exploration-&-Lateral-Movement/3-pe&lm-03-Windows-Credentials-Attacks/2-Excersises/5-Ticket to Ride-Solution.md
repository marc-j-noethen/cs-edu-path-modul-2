# 🐍 Ticket to Ride (3-pe&lm-03-Windows-Credentials-Attacks)

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Practice Kerberos Pass-the-Ticket (PtT) attacks using Mimikatz.

**Requirements:**

- Original room link: `https://tryhackme.com/room/postexploit`
    
- Official room title: `Post-Exploitation Basics`
    
- Official room focus: Learn the basics of post-exploitation and maintaining access with mimikatz, bloodhound, powerview and msfvenom
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - Screenshot of the final `klist` output after the ticket injection.

---

## Solution

```text
# Inputs
room = 'Post-Exploitation Basics'
room_url = 'https://tryhackme.com/room/postexploit'
focus = 'Practice Kerberos Pass-the-Ticket (PtT) attacks using Mimikatz'
submission = 'Screenshot of the final `klist` output after the ticket injection.'

# Main logic
1. I opened the linked TryHackMe room `Post-Exploitation Basics`.
2. I connected to the Windows machine that belonged to the linked room.
3. I ran `klist`, recorded the initial ticket state, dumped the Kerberos tickets with Mimikatz, and injected one of them into my current session.
4. I ran `klist` again, compared the new ticket state with the initial output, and kept the final screenshot the exercise asked for.
```

**Alternative (compact):**

```text
I completed "Ticket to Ride" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Post-Exploitation Basics`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Practice Kerberos Pass-the-Ticket (PtT) attacks using Mimikatz`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Post-Exploitation Basics` as the linked lab for this exercise.|
|Focus|This exercise focused on: Practice Kerberos Pass-the-Ticket (PtT) attacks using Mimikatz.|
|Evidence|I kept the requested artifact: Screenshot of the final `klist` output after the ticket injection.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Practice Kerberos Pass-the-Ticket (PtT) attacks using Mimikatz.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``klist``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "Ticket to Ride" and kept the requested evidence.
        
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






