# Asymmetric Encryption and Diffie-Hellman Key Exchange

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains public-key cryptography, digital signatures, and key exchange concepts such as Diffie-Hellman.

### 2. Key ideas
- Asymmetric cryptography uses a public key and a private key with different security roles.
- Public-key encryption helps solve key distribution problems, but it is usually slower than symmetric encryption.
- Diffie-Hellman and ECDH allow two parties to derive a shared secret over an untrusted channel.
- Key exchange alone does not provide authentication, which is why certificates or other trust mechanisms are still needed.

### 3. Tools and practical relevance
- OpenSSL is commonly used in labs to inspect keys, signatures, and certificate-related data.
- OpenSSH is a practical real-world example of public-key authentication.

### 4. Key takeaway
Modern secure systems usually combine asymmetric methods for trust and setup with symmetric methods for bulk data protection.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| OpenSSL | Inspect keys, signatures, and crypto operations in lab settings |
| OpenSSH | Real-world example of public-key authentication and secure remote access |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Public key | Key that may be shared openly |
| Private key | Secret key that must remain protected |
| Digital signature | Cryptographic proof of integrity and origin |
| Diffie-Hellman | Method for deriving a shared secret over an insecure channel |
| ECDH | Elliptic-curve version of Diffie-Hellman |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| pair | two cryptographically related keys |
| exchange | process of establishing a shared secret |
| authenticate | prove identity or origin |
| sign | create a digital signature |
| verify | confirm a signature or proof |
