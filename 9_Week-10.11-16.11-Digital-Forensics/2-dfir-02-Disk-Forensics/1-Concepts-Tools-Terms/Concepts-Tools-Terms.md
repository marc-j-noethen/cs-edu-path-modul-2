# Disk Forensics

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how investigators examine storage media to recover files, timelines, metadata, and user activity evidence.

### 2. Key ideas
- Disk forensics focuses on persistent data stored on drives and disk images.
- Important evidence often comes from file systems, timestamps, deleted files, browser artifacts, logs, and application traces.
- Investigators should work from forensic copies rather than directly from original media whenever possible.
- Time interpretation matters because local time, UTC, and clock drift can all affect conclusions.

### 3. Tools and practical relevance
- Imaging tools help acquire disks safely.
- Forensic suites help parse file systems, metadata, and deleted content.

### 4. Key takeaway
Disk evidence is rich, but it only becomes useful when it is preserved carefully and interpreted in context.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Forensic imaging tool | Create a bit-level copy of a drive or partition |
| Autopsy or similar suite | Analyze file systems and artifacts |
| Hashing tools | Verify image integrity before and after analysis |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Disk image | Forensic copy of storage media |
| File system | Structure used to organize stored files |
| Metadata | Data about files such as timestamps or ownership |
| Deleted file recovery | Attempt to recover content that is no longer linked normally |
| Timeline analysis | Ordering events based on artifact timestamps |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| image | copy of storage content |
| sector | low-level storage unit |
| timestamp | recorded date and time value |
| recover | retrieve lost or hidden data |
| mount | attach a file system for access |
