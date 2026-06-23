# Memory Forensics

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how volatile memory can reveal running processes, active connections, injected code, and other evidence not visible on disk.

### 2. Key ideas
- Memory is volatile, so capture timing matters.
- RAM can reveal running malware, process relationships, network connections, command history, and decrypted material that may never be written to disk.
- Memory forensics is especially valuable when attackers use fileless or short-lived techniques.
- Analysis results are strongest when they are correlated with disk and log evidence.

### 3. Tools and practical relevance
- Memory acquisition tools capture RAM for later analysis.
- Volatility-style frameworks help parse memory structures and extract evidence.

### 4. Key takeaway
If you wait too long, memory evidence disappears. Volatile data often contains the clearest picture of what was happening right now.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Memory acquisition tool | Capture RAM from a live system |
| Volatility | Analyze memory images for processes, connections, and artifacts |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| RAM | Volatile memory used by a running system |
| Memory image | Captured copy of system memory |
| Fileless activity | Behavior that relies more on memory than on persistent files |
| Injected code | Code inserted into another process's memory space |
| Volatile evidence | Evidence that disappears when power is lost or state changes |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| capture | collect a snapshot for analysis |
| volatile | short-lived and easily lost |
| process | running program instance |
| connection | active communication path |
| artifact | trace left in memory |
