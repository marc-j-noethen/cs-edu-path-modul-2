# 🐍 RSAU

**Course:** Cyber Security Analyst - Asymmetric Encryption & Diffie Hellman | **Date:** 07 October 2025

---

## Task

**Goal:**  
Implement the core mathematical logic of RSA key generation, encryption, and decryption in Python without relying on high-level crypto libraries for the core operations.

**Requirements:**

- **Modular Inverse:** The most crucial helper function you need is for the modular multiplicative inverse. Research and implement the **Extended Euclidean Algorithm** to create a function `invmod(e, et)` that finds `d`.
    
- **Key Generation:**
    
- Write a function `generate_keys()`.
    
- For simplicity, start with two small prime numbers, e.g., `p = 61` and `q = 53`.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
def egcd(a, b):
    if b == 0:
        return a, 1, 0
    g, x1, y1 = egcd(b, a % b)
    return g, y1, x1 - (a // b) * y1


def invmod(e, et):
    g, x, _ = egcd(e, et)
    if g != 1:
        raise ValueError("No modular inverse exists")
    return x % et


def generate_keys():
    p = 61
    q = 53
    n = p * q
    et = (p - 1) * (q - 1)
    e = 17
    d = invmod(e, et)
    public_key = (e, n)
    private_key = (d, n)
    return public_key, private_key


def verschluesseln(public_key, klartext):
    e, n = public_key
    return [pow(ord(char), e, n) for char in klartext]


def entschluesseln(private_key, ciphertext_list):
    d, n = private_key
    return "".join(chr(pow(block, d, n)) for block in ciphertext_list)


if __name__ == "__main__":
    public_key, private_key = generate_keys()
    message = "Hallo RSA!"
    ciphertext = verschluesseln(public_key, message)
    decrypted = entschluesseln(private_key, ciphertext)

    print("Public key:", public_key)
    print("Private key:", private_key)
    print("Ciphertext:", ciphertext)
    print("Decrypted:", decrypted)
```








