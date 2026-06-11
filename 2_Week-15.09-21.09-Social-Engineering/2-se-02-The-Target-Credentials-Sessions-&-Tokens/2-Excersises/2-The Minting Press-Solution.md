# 🐍 The Minting Press 

**Course:** Cyber Security Analyst - Sessions & Tokens | **Date:** 16 September 2025

---

## Task

**Goal:**  
Build a simple Flask API that correctly issues and validates JSON Web Tokens (JWTs) to protect a specific endpoint.

**Requirements:**

- Has a public endpoint `/` that returns a simple welcome message.
    
- Has a `/login` endpoint that accepts a POST request with a dummy `username` and `password`. If they match a hardcoded value, it should generate a JWT.
    
- The JWT payload must contain the `username` and an expiration time (`exp`) set to 5 minutes in the future.
    
- It should return the JWT to the user.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
from datetime import datetime, timedelta, timezone

import jwt
from flask import Flask, jsonify, request


app = Flask(__name__)
app.secret_key = "jwt-demo-secret"

JWT_SECRET = "jwt-demo-secret"
USERNAME = "user"
PASSWORD = "password"


@app.route("/")
def index():
    return jsonify(message="Welcome to the JWT demo")


@app.route("/login", methods=["POST"])
def login():
    data = request.get_json(silent=True) or request.form
    if data.get("username") == USERNAME and data.get("password") == PASSWORD:
        payload = {
            "username": USERNAME,
            "exp": datetime.now(timezone.utc) + timedelta(minutes=5),
        }
        token = jwt.encode(payload, JWT_SECRET, algorithm="HS256")
        if isinstance(token, bytes):
            token = token.decode("utf-8")
        return jsonify(token=token)

    return jsonify(error="Unauthorized"), 401


@app.route("/protected")
def protected():
    auth_header = request.headers.get("Authorization", "")
    if not auth_header.startswith("Bearer "):
        return jsonify(error="Unauthorized"), 401

    token = auth_header.removeprefix("Bearer ").strip()
    try:
        payload = jwt.decode(token, JWT_SECRET, algorithms=["HS256"])
    except jwt.ExpiredSignatureError:
        return jsonify(error="Token expired"), 401
    except jwt.InvalidTokenError:
        return jsonify(error="Unauthorized"), 401

    return jsonify(message=f"Willkommen {payload['username']}, Sie haben Zugriff!")


if __name__ == "__main__":
    app.run(host="127.0.0.1", port=5000, debug=True)
```


