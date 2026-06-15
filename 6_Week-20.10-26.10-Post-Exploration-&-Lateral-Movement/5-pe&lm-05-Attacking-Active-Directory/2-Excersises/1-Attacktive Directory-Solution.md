# comment all ines with old "nameserver" addresses with #

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Successfully complete the "Attacktive Directory" TryHackMe room.

**Requirements:**

- Original room link: `https://tryhackme.com/room/attacktivedirectory`
    
- Official room title: `Attacktive Directory`
    
- Official room focus: Successfully complete the "Attacktive Directory" TryHackMe room.
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - Submit a screenshot showing the completed room

---

## Solution

```text
# Inputs
room = 'Attacktive Directory'
room_url = 'https://tryhackme.com/room/attacktivedirectory'
focus = 'Successfully complete the "Attacktive Directory" TryHackMe room'
submission = 'Submit a screenshot showing the completed room'

# Main logic
1. I opened the linked TryHackMe room `Attacktive Directory`.
2. I completed the linked TryHackMe room `Attacktive Directory`.
3. On an ARM-based local Kali setup, I compiled `kerbrute` from source because the prebuilt binary was not available.
4. When local DNS resolution caused problems, I corrected the resolver configuration and then kept the requested room-completion screenshot as evidence.
```

**Alternative (compact):**

```text
I completed "Attacktive Directory" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Attacktive Directory`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Successfully complete the "Attacktive Directory" TryHackMe room`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Attacktive Directory` as the linked lab for this exercise.|
|Focus|This exercise focused on: Successfully complete the "Attacktive Directory" TryHackMe room.|
|Evidence|I kept the requested artifact: Submit a screenshot showing the completed room.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Successfully complete the "Attacktive Directory" TryHackMe room.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``jsx cd ~/Downloads sudo apt update sudo apt install -y golang-go git clone <https://github.com/ropnop/kerbrute.git> kerbrute-source cd kerbrute-source go build -o kerbrute . mv kerbrute ~/Downloads/ cd ~/Downloads chmod +x kerbrute #check if it works: ./kerbrute --help ``, `` If you get an error “no such host”, you might need to configure your dns. Edit ``, `` : ``, ``jsx sudo nano /etc/resolv.conf # comment all ines with old "nameserver" addresses with # # add these line at the beginning: nameserver 8.8.8.8 nameserver 8.8.4.4 ``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "Attacktive Directory" and kept the requested evidence.
        
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






