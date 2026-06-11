# 🐍 Cracked 

**Course:** Cyber Security Analyst - Social Engineering | **Date:** 15 September 2025

---

## Task

**Goal:**  
Write your own basic password cracker in Python and compare its performance against an optimized tool like John the Ripper or Hashcat.

**Requirements:**

- Accept two command-line arguments: the MD5 hash to crack and the path to a wordlist file.
    
- For each word in the wordlist, it should hash the word using MD5 and compare it to the target hash.
    
- If a match is found, it should print the cracked password and the time it took to find it, then exit.
    
- If the wordlist is exhausted, it should report that the password was not found.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
import hashlib
import sys
import time


def crack_md5(target_hash: str, wordlist_path: str):
    start = time.perf_counter()

    with open(wordlist_path, "r", encoding="utf-8", errors="ignore") as handle:
        for line in handle:
            candidate = line.strip()
            if hashlib.md5(candidate.encode("utf-8")).hexdigest() == target_hash.lower():
                elapsed = time.perf_counter() - start
                print(f"Password found: {candidate}")
                print(f"Time to crack: {elapsed:.4f} seconds")
                return candidate

    elapsed = time.perf_counter() - start
    print("Password not found")
    print(f"Time spent: {elapsed:.4f} seconds")
    return None


if __name__ == "__main__":
    if len(sys.argv) != 3:
        raise SystemExit("Usage: python cracker.py <md5-hash> <wordlist>")

    crack_md5(sys.argv[1], sys.argv[2])
```

**Part 2**

- The MD5 hash for `Superman2007` can be generated with:

```bash
python -c "import hashlib; print(hashlib.md5(b'Superman2007').hexdigest())"
```

- `John the Ripper` or `Hashcat` are usually much faster than the Python script because they are compiled, heavily optimized, and can use multiple CPU cores or GPUs.
- The simple Python cracker is fine for learning and very small wordlists, but it is not competitive for real cracking workloads.


