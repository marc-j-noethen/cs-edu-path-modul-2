# 🐍 The Bouncer 

**Course:** Cyber Security Analyst - Social Engineering | **Date:** 15 September 2025

---

## Task

**Goal:**  
Implement a secure user registration and login system in Python using modern password hashing techniques.

**Requirements:**

- `register(username, password)`:
    
- This function should take a username and password.
    
- It must use the `bcrypt` library to generate a salted hash of the password.
    
- It should store the username and the hashed password in your user dictionary.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
import bcrypt


users = {}


def register(username: str, password: str) -> bytes:
    hashed_password = bcrypt.hashpw(password.encode("utf-8"), bcrypt.gensalt())
    users[username] = hashed_password
    return hashed_password


def login(username: str, password: str) -> bool:
    stored_hash = users.get(username)
    if stored_hash is None:
        return False
    return bcrypt.checkpw(password.encode("utf-8"), stored_hash)


if __name__ == "__main__":
    print("Registered hash:", register("alice", "P@ssw0rd!").decode("utf-8"))
    print("Login with correct password:", login("alice", "P@ssw0rd!"))
    print("Login with wrong password:", login("alice", "wrong-password"))
```


