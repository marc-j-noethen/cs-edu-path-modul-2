# 🐍 Diffie-Hellman-You

**Course:** Cyber Security Analyst - Asymmetric Encryption & Diffie Hellman | **Date:** 07 October 2025

---

## Task

**Goal:**  
Implement the Diffie-Hellman key exchange protocol in Python to establish a shared secret between two parties without that secret ever crossing the wire.

**Requirements:**

- **Part 1: The Basics**
    
- In your scripts, set the public parameters `p = 37` and `g = 5`.
    
- In `alice.py`, generate a random secret integer `a`. Calculate her public value `A = (g**a) % p`.
    
- In `bob.py`, generate a random secret integer `b`. Calculate his public value `B = (g**b) % p`.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

### `alice.py`

```python
import argparse
import secrets


NAME = "Alice"
p = int(
    "ffffffffffffffffc90fdaa22168c234c4c6628b80dc1cd129024e088a67cc74020bbea63b139b22514a08798e3404ddef9519b3cd3a431b302b0a6df25f14374fe1356d6d51c245e485b576625e7ec6f44c42e9a637ed6b0bff5cb6f406b7edee386bfb5a899fa5ae9f24117c4b1fe649286651ece45b3dc2007cb8a163bf0598da48361c55d39a69163fa8fd24cf5f83655d23dca3ad961c62f356208552bb9ed529077096966d670c354e4abc9804f1746c08ca237327ffffffffffffffff",
    16,
)
g = 2


def main():
    parser = argparse.ArgumentParser()
    parser.add_argument("--secret", type=int, default=None, help="Optional fixed private value for repeatable demos")
    parser.add_argument("--peer", type=int, required=False, help="Peer public value")
    args = parser.parse_args()

    secret = args.secret if args.secret is not None else secrets.randbelow(p - 2) + 2
    public_value = pow(g, secret, p)

    print(f"{NAME} secret: {secret}")
    print(f"{NAME} public value: {public_value}")

    if args.peer is not None:
        shared_secret = pow(args.peer, secret, p)
        print(f"{NAME} shared secret: {shared_secret}")


if __name__ == "__main__":
    main()
```

### `bob.py`

```python
import argparse
import secrets


NAME = "Bob"
p = int(
    "ffffffffffffffffc90fdaa22168c234c4c6628b80dc1cd129024e088a67cc74020bbea63b139b22514a08798e3404ddef9519b3cd3a431b302b0a6df25f14374fe1356d6d51c245e485b576625e7ec6f44c42e9a637ed6b0bff5cb6f406b7edee386bfb5a899fa5ae9f24117c4b1fe649286651ece45b3dc2007cb8a163bf0598da48361c55d39a69163fa8fd24cf5f83655d23dca3ad961c62f356208552bb9ed529077096966d670c354e4abc9804f1746c08ca237327ffffffffffffffff",
    16,
)
g = 2


def main():
    parser = argparse.ArgumentParser()
    parser.add_argument("--secret", type=int, default=None, help="Optional fixed private value for repeatable demos")
    parser.add_argument("--peer", type=int, required=False, help="Peer public value")
    args = parser.parse_args()

    secret = args.secret if args.secret is not None else secrets.randbelow(p - 2) + 2
    public_value = pow(g, secret, p)

    print(f"{NAME} secret: {secret}")
    print(f"{NAME} public value: {public_value}")

    if args.peer is not None:
        shared_secret = pow(args.peer, secret, p)
        print(f"{NAME} shared secret: {shared_secret}")


if __name__ == "__main__":
    main()
```

### Example use

```bash
python alice.py --secret 12345 --peer <bob-public>
python bob.py --secret 67890 --peer <alice-public>
```








