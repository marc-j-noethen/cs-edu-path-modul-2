# 🐍 ECB Under The Sea

**Course:** Cyber Security Analyst - Symmetric Encryption & Hashing | **Date:** 06 October 2025

---

## Task

**Goal:**  
Write a Python script to decrypt a file encrypted with AES-128 in ECB mode.

**Requirements:**

- The following file was encrypted using AES-128 in ECB mode and Base64-encoded.
    
- The key is `"YELLOW SUBMARINE"`.
    
- [encrypted_YELLOW SUBMARINE.txt](attachment:9341aa9d-f1a1-4372-b4d6-33b74bbb2afc:encrypted_YELLOW_SUBMARINE.txt)

Your task is to write a Python script that decrypts the file.
    
- You have the key, after all.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
from base64 import b64decode
from pathlib import Path

from cryptography.hazmat.primitives import padding
from cryptography.hazmat.primitives.ciphers import Cipher, algorithms, modes


key = b"YELLOW SUBMARINE"
ciphertext_b64 = Path("encrypted_YELLOW_SUBMARINE.txt").read_text(encoding="utf-8").strip()
ciphertext = b64decode(ciphertext_b64)

decryptor = Cipher(algorithms.AES(key), modes.ECB()).decryptor()
padded_plaintext = decryptor.update(ciphertext) + decryptor.finalize()

unpadder = padding.PKCS7(128).unpadder()
plaintext = unpadder.update(padded_plaintext) + unpadder.finalize()

print(plaintext.decode("utf-8"))
```


