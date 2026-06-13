# 🐍 Cryptographic Kintsugi 

**Course:** Cyber Security Analyst - Asymmetric Encryption & Diffie Hellman | **Date:** 07 October 2025

---

## Task

**Goal:**  
This is a challenge to deepen your understanding of how RSA keys work internally. You will reconstruct a full RSA private key from its fundamental mathematical components and then use it to decrypt a message.

**Requirements:**

- **p**: `10296599936259208241298667469090738973330021100274129160139135417603909739559483849736960531800183423438566578726663779072952716734185656873863275475768303`
    
- **q**: `6954142120272676728168305582939505734988346986071535073551877726313275941908217695745604456051882544532039300139096390348220491195204680587673668713338467`
    
- **e**: `65537`
    
- **Research:** Figure out how an RSA private key is constructed. You know `p`, `q`, and `e`. What other numbers do you need to calculate (like `d`, `dmp1`, `dmq1`, `iqmp`) to build a complete private key?
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
from base64 import b64decode
from pathlib import Path

from cryptography.hazmat.primitives import serialization
from cryptography.hazmat.primitives.asymmetric import rsa
from cryptography.hazmat.primitives.asymmetric.padding import OAEP, MGF1
from cryptography.hazmat.primitives.hashes import SHA256


p = 10296599936259208241298667469090738973330021100274129160139135417603909739559483849736960531800183423438566578726663779072952716734185656873863275475768303
q = 6954142120272676728168305582939505734988346986071535073551877726313275941908217695745604456051882544532039300139096390348220491195204680587673668713338467
e = 65537

n = p * q
phi = (p - 1) * (q - 1)
d = pow(e, -1, phi)
dmp1 = d % (p - 1)
dmq1 = d % (q - 1)
iqmp = pow(q, -1, p)

private_numbers = rsa.RSAPrivateNumbers(
    p=p,
    q=q,
    d=d,
    dmp1=dmp1,
    dmq1=dmq1,
    iqmp=iqmp,
    public_numbers=rsa.RSAPublicNumbers(e=e, n=n),
)
private_key = private_numbers.private_key()

pem = private_key.private_bytes(
    encoding=serialization.Encoding.PEM,
    format=serialization.PrivateFormat.TraditionalOpenSSL,
    encryption_algorithm=serialization.NoEncryption(),
)
Path("reconstructed_private_key.pem").write_bytes(pem)
print("Wrote reconstructed_private_key.pem")
```

### OpenSSL decrypt command

```bash
base64 -d final_message.enc.b64 > final_message.enc
openssl pkeyutl -decrypt -inkey reconstructed_private_key.pem -in final_message.enc -out final_message.txt -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256
```

### Final message

`Top Secret Message`








