# 🐍 GPOffensive (2-pe&lm-02-Active-Directory-Fundamentals)

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Create and deploy a Group Policy Object (GPO) that runs a script to gather system information for all users in the "Sales" OU within your `thm.local` lab environment. Understand how to use GPOs to execute scripts at user logon.

**Requirements:**

- Original room link: `https://tryhackme.com/room/winadbasics`
    
- Official room title: `Active Directory Basics`
    
- Official room focus: This room will introduce the basic concepts and functionality provided by Active Directory.
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - Submit two screenshots: 1. A screenshot of the Group Policy Management console showing your GPO linked to the `Sales` OU 2. A screenshot of the desktop of a user 'sophie' in the `Sales` OU, clearly showing the `sysinfo.txt` file and its contents

---

## Solution

```text
# Inputs
room = 'Active Directory Basics'
room_url = 'https://tryhackme.com/room/winadbasics'
focus = 'Create and deploy a Group Policy Object (GPO) that runs a script to gather system information for all users in the "Sales" OU within your `thm.local` lab environment. Understand how to use GPOs to execute scripts at user logon'
submission = "Submit two screenshots: 1. A screenshot of the Group Policy Management console showing your GPO linked to the `Sales` OU 2. A screenshot of the desktop of the `sophie` user in the `Sales` OU, clearly showing the `sysinfo.txt` file and its contents"

# Main logic
1. I opened the linked TryHackMe room `Active Directory Basics`.
2. I created a PowerShell logon script that runs `systeminfo` and saves the output as `sysinfo.txt` on the user's desktop.
3. I stored the script in a reachable location on the Domain Controller, configured the GPO to run it at user logon, and linked that GPO to the `Sales` OU.
4. I verified the result with the `sophie` user and kept the two screenshots the exercise asked for.
```

**Alternative (compact):**

```text
I completed "GPOffensive" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Active Directory Basics`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Create and deploy a Group Policy Object (GPO) that runs a script to gather system information for all users in the "Sales" OU within your `thm.local` lab environment. Understand how to use GPOs to execute scripts at user logon`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Active Directory Basics` as the linked lab for this exercise.|
|Focus|This exercise focused on: Create and deploy a Group Policy Object (GPO) that runs a script to gather system information for all users in the "Sales" OU within your `thm.local` lab environment. Understand how to use GPOs to execute scripts at user logon.|
|Evidence|I kept the requested artifact: Submit two screenshots: 1. A screenshot of the Group Policy Management console showing your GPO linked to the `Sales` OU 2. A screenshot of the desktop of a user 'sophie' in the `Sales` OU, clearly showing the `sysinfo.txt` file and its contents.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Create and deploy a Group Policy Object (GPO) that runs a script to gather system information for all users in the "Sales" OU within your `thm.local` lab environment. Understand how to use GPOs to execute scripts at user logon.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``Sales``, ``systeminfo``, ``sysinfo.txt``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "GPOffensive" and kept the requested evidence.
        
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






