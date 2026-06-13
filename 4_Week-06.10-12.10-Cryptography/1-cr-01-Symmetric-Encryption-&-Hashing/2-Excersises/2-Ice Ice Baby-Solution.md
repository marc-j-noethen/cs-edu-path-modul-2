# 🐍 Ice Ice Baby 

**Course:** Cyber Security Analyst - Symmetric Encryption & Hashing | **Date:** 06 October 2025

---

## Task

**Goal:**  
Implement the repeating-key XOR encryption algorithm in Python.

**Requirements:**

- In repeating-key XOR, you sequentially apply each byte of the key to the plaintext.
    
- For a key "ICE", the first byte of plaintext is XOR'd with 'I', the second with 'C', the third with 'E', the fourth with 'I' again, and so on.
    
- Write a Python script that takes a string of plaintext and a key, and produces the hex-encoded encrypted output.
    
- Encrypt the following text with the key "ICE":

```
Burning 'em, if you ain't quick and nimble
I go crazy when I hear a cymbal
```

Your script should produce the following output:`0b3637272a2b2e63622c2e69692a23693a2a3c6324202d623d63343c2a26226324272765272a282b2f20430a652e2c652a3124333a653e2b2027630c692b20283165286326302e27282f`
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
from itertools import cycle


def repeating_key_xor(plaintext: str, key: str) -> str:
    plaintext_bytes = plaintext.encode("utf-8")
    key_bytes = key.encode("utf-8")
    ciphertext = bytes(byte ^ key_byte for byte, key_byte in zip(plaintext_bytes, cycle(key_bytes)))
    return ciphertext.hex()


plaintext = """Burning 'em, if you ain't quick and nimble
I go crazy when I hear a cymbal"""

print(repeating_key_xor(plaintext, "ICE"))
```


