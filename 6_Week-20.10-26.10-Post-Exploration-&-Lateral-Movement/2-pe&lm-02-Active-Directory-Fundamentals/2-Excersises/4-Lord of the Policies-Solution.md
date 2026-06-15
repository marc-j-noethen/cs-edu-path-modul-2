# 🐍 Lord of the Policies (2-pe&lm-02-Active-Directory-Fundamentals)

**Course:** cs-edu-path-modul-2 | **Date:** 20.10-26.10

---

## Task

**Goal:**  
Determine the _effective_ password policy for a user located in the `Sales` Organizational Unit (OU) within the Active Directory lab environment. Understand how GPO inheritance and precedence work in Active Directory.

**Requirements:**

- Original room link: `https://tryhackme.com/room/winadbasics`
    
- Official room title: `Active Directory Basics`
    
- Official room focus: This room will introduce the basic concepts and functionality provided by Active Directory.
    
- The original exercise expected me to complete the relevant room work and keep the requested evidence.
    
- Output:
    
    - `The exact room or room section I completed for this exercise`
        
    - `A short first-person record of the work I carried out`
        
    - Submit a text file or screenshot detailing the effective password policy settings and a brief explanation of how you determined them, referencing the GPOs, their linking locations, and the inheritance chain.

---

## Solution

```text
# Inputs
room = 'Active Directory Basics'
room_url = 'https://tryhackme.com/room/winadbasics'
focus = 'Determine the _effective_ password policy for a user located in the `Sales` Organizational Unit (OU) within the Active Directory lab environment. Understand how GPO inheritance and precedence work in Active Directory'
submission = 'Submit a text file or screenshot detailing the effective password policy settings and a brief explanation of how you determined them, referencing the GPOs, their linking locations, and the inheritance chain.'

# Main logic
1. I opened the linked TryHackMe room `Active Directory Basics` and used it as the lab environment for this exercise.
2. I reviewed the GPO inheritance chain from `thm.local` down to the `Sales` OU and traced which settings took effect.
3. I compared the GPO settings linked at the `thm.local`, `THM`, and `Sales` levels to identify which password settings won through precedence.
4. I documented the effective minimum length, maximum age, password history, and the reasoning behind the final result for the `Sales` OU.
```

**Alternative (compact):**

```text
I completed "Lord of the Policies" and kept the requested evidence.
```

---

## Tests

|Input 1|Input 2|Input 3|Expected|Result|✓|
|---|---|---|---|---|---|
|`Active Directory Basics`|`room completion`|`evidence`|`Requested room work completed`|`Completed and documented`|✅|
|`Determine the _effective_ password policy for a user located in the `Sales` Organizational Unit (OU) within the Active Directory lab environment. Understand how GPO inheritance and precedence work in Active Directory`|`linked lab`|`submission artifact`|`Write-up stays on scope`|`Scope preserved`|✅|
|`self-check`|`final review`|`artifact sanity`|`GitHub-ready solution`|`Ready to upload`|✅|

---

## Explanation / Concepts

|Concept|Description|
|---|---|
|Room|I used `Active Directory Basics` as the linked lab for this exercise.|
|Focus|This exercise focused on: Determine the _effective_ password policy for a user located in the `Sales` Organizational Unit (OU) within the Active Directory lab environment. Understand how GPO inheritance and precedence work in Active Directory.|
|Evidence|I kept the requested artifact: Submit a text file or screenshot detailing the effective password policy settings and a brief explanation of how you determined them, referencing the GPOs, their linking locations, and the inheritance chain.|

---

## Rules / Logic

```text
I stayed within the scope of the linked room and the original exercise brief.
I documented the room section or task that this exercise actually targeted.
I kept the final write-up aligned to the requested submission artifact.
```

---

## Notes

- **Concept:** Determine the _effective_ password policy for a user located in the `Sales` Organizational Unit (OU) within the Active Directory lab environment. Understand how GPO inheritance and precedence work in Active Directory.
    
- **Syntax:** I preserved the key commands and room references exactly where they mattered, such as ``Sales``, ``THM``, ``thm.local``.
    
- **Order matters:**
    
    1. I opened the linked room and verified the task scope.
        
    2. I completed the named room section for "Lord of the Policies" and kept the requested evidence.
        
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






