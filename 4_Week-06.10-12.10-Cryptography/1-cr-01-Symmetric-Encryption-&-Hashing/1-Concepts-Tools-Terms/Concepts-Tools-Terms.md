# Symmetric Encryption and Hashing

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains two core building blocks of applied cryptography: symmetric encryption for confidentiality and hashing for integrity-related use cases.

### 2. Key ideas
- Symmetric encryption uses one shared secret key for encryption and decryption.
- Hash functions are one-way operations that produce a fixed-length digest from input data.
- Encryption hides content; hashing does not hide content and cannot be reversed to recover plaintext.
- Password storage should use slow, salted password hashing schemes such as Argon2id, bcrypt, scrypt, or PBKDF2 rather than plain fast hashes.

### 3. Tools and practical relevance
- CyberChef is useful for safe lab experiments with encoding, hashing, and basic crypto transformations.
- OpenSSL and similar command-line tools are common for encryption and digest demonstrations.

### 4. Key takeaway
Encryption protects secrecy, while hashing helps with verification and password storage workflows. They solve different problems.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| CyberChef | Safe browser-based lab tool for encoding, hashing, and crypto experiments |
| OpenSSL | Command-line toolkit for encryption, certificates, and digests |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Symmetric encryption | Encryption that uses the same secret key for both directions |
| Hash function | One-way algorithm that produces a digest from input |
| Salt | Random value added before password hashing to prevent identical hashes |
| Integrity | Assurance that data has not been changed unexpectedly |
| Confidentiality | Protection of data against unauthorized disclosure |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| secret key | shared value used for encryption and decryption |
| digest | fixed-length hash output |
| plaintext | original readable data |
| ciphertext | encrypted data |
| verify | check whether data matches an expected value |
