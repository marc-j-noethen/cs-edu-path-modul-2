# Mimi Blocked

**Course:** Cyber Security Analyst - Windows Credentials Attacks | **Date:** 22 October 2025

---

## Task

**Goal:**  
Observe how endpoint security reacts to downloading Mimikatz on a local Windows VM and research common AV/EDR bypass techniques.

**Requirements:**

- Use your local Windows VM, not the TryHackMe VM.
- Open the official Mimikatz releases page on GitHub.
- Observe any Defender alert, block, quarantine, or protection-history entry.
- Research three common techniques attackers use to bypass endpoint security.

---

## Solution

I used the official Mimikatz releases page on my local Windows VM with Defender enabled. The download attempt was blocked or flagged by Windows Defender, and any detection would appear in Protection History or Quarantine.

Three common bypass techniques I researched were:

- Obfuscation or packing: rename or pack the binary to change its signature.
- Security control tampering: disable or interfere with Defender, AMSI, ETW, or related telemetry before execution.
- Fileless or memory-only execution: load the payload into memory or use living-off-the-land techniques instead of dropping a normal executable to disk.
