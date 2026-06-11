# 🐍 Self-Hijack 

**Course:** Cyber Security Analyst - Sessions & Tokens | **Date:** 16 September 2025

---

## Task

**Goal:**  
Build a simple Flask web application that uses session cookies for authentication, and then perform a session hijacking attack against your own application.

**Requirements:**

- Read the task carefully and identify the exact objective.
    
- Apply the correct concept, method, or platform workflow.
    
- Validate the final result against the stated goal.
    
- Submit only the evidence or answer format requested.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
from flask import Flask, redirect, render_template_string, request, session, url_for


app = Flask(__name__)
app.secret_key = "session-cookie-demo"

users = {"user": "password"}

LOGIN_TEMPLATE = """
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Login</title>
  </head>
  <body>
    <h1>Login</h1>
    <form method="post">
      <label>Username <input name="username"></label><br>
      <label>Password <input name="password" type="password"></label><br>
      <button type="submit">Login</button>
    </form>
  </body>
</html>
"""


@app.route("/", methods=["GET", "POST"])
def login():
    if request.method == "POST":
        username = request.form.get("username", "")
        password = request.form.get("password", "")

        if users.get(username) == password:
            session["user"] = username
            return redirect(url_for("protected"))

        return "Invalid credentials", 401

    return render_template_string(LOGIN_TEMPLATE)


@app.route("/protected")
def protected():
    username = session.get("user")
    if not username:
        return redirect(url_for("login"))
    return f"Willkommen, {username}!"


if __name__ == "__main__":
    app.run(host="127.0.0.1", port=5000, debug=True)
```

### Run it

```bash
python my_app.py
```


