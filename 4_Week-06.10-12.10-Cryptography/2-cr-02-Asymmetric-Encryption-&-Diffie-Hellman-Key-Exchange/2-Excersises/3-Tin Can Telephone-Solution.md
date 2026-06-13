# 🐍 Tin Can Telephone 

**Course:** Cyber Security Analyst - Asymmetric Encryption & Diffie Hellman | **Date:** 07 October 2025

---

## Task

**Goal:**  
Implement a simple, two-way secure messaging protocol in Python. You will create a `client` that sends a signed, secret message and a `server` that validates it.

**Requirements:**

- First, ensure you have the library installed: `pip install cryptography`.
    
- Generate two key pairs using `openssl`:
    
- One for the "client": `client_private.pem`, `client_public.pem`.
    
- One for the "server": `server_private.pem`, `server_public.pem`.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

### `client.py`

```python
from pathlib import Path

from cryptography.hazmat.primitives import hashes, serialization
from cryptography.hazmat.primitives.asymmetric import padding


SECRET_MESSAGE = b"Der Adler ist gelandet."

with open("client_private.pem", "rb") as handle:
    client_private_key = serialization.load_pem_private_key(handle.read(), password=None)

with open("server_public.pem", "rb") as handle:
    server_public_key = serialization.load_pem_public_key(handle.read())

signature = client_private_key.sign(SECRET_MESSAGE)
package = SECRET_MESSAGE + signature

ciphertext = server_public_key.encrypt(
    package,
    padding.OAEP(
        mgf=padding.MGF1(algorithm=hashes.SHA256()),
        algorithm=hashes.SHA256(),
        label=None,
    ),
)

Path("package.enc").write_bytes(ciphertext)
print("client.py: wrote package.enc")
```

### `server.py`

```python
from pathlib import Path

from cryptography.hazmat.primitives import hashes, serialization
from cryptography.hazmat.primitives.asymmetric import padding


SECRET_MESSAGE = b"Der Adler ist gelandet."

with open("server_private.pem", "rb") as handle:
    server_private_key = serialization.load_pem_private_key(handle.read(), password=None)

with open("client_public.pem", "rb") as handle:
    client_public_key = serialization.load_pem_public_key(handle.read())

ciphertext = Path("package.enc").read_bytes()
payload = server_private_key.decrypt(
    ciphertext,
    padding.OAEP(
        mgf=padding.MGF1(algorithm=hashes.SHA256()),
        algorithm=hashes.SHA256(),
        label=None,
    ),
)

message = payload[: len(SECRET_MESSAGE)]
signature = payload[len(SECRET_MESSAGE) :]

client_public_key.verify(signature, message)
print("Server: Client-Signatur ist gültig! Nachricht erhalten.")
print(message.decode("utf-8"))
```

### OpenSSL key generation

```bash
openssl genpkey -algorithm Ed25519 -out client_private.pem
openssl pkey -in client_private.pem -pubout -out client_public.pem
openssl genpkey -algorithm RSA -pkeyopt rsa_keygen_bits:2048 -out server_private.pem
openssl pkey -in server_private.pem -pubout -out server_public.pem
```








