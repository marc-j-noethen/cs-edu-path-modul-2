# Evilginx2 Lab Entries

**Course:** Cyber Security Analyst - Advanced Phishing & MFAPC | **Date:** 18 September 2025

---

## Task

**Goal:**  
Set up a simulated Adversary-in-the-Middle (AiTM) phishing environment on Kali machine using Evilginx2. You will execute an attack against one of your own online accounts to understand how credentials and session tokens can be intercepted, even when MFA is active.

<aside> ⚠️

This is a hands-on exercise using a real phishing tool in a controlled, local environment. You will **only** target an account that you own for educational purposes. Using this tool against any person or system without explicit, written permission is illegal and unethical.

</aside>

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

### Commands and setup

- Edit `/etc/hosts` so the chosen phishing domain resolves to `127.0.0.1`.
- Start Evilginx2 in developer mode for local testing.
- Configure the fake domain and local IP.
- Enable the chosen phishlet and create a lure URL.
- Open the lure in a browser, sign in with your own account, and confirm that the terminal shows captured credentials or session data.

### How Evilginx works

Evilginx2 sits between the victim and the legitimate service as a reverse proxy. It relays the login flow to the real site, captures credentials, and can also capture session cookies, which is why MFA alone does not stop a session hijack.

### Detection and prevention

- Prefer phishing-resistant MFA such as FIDO2 or WebAuthn.
- Add conditional access, device checks, and risk-based sign-in policies.
- Monitor for suspicious proxy indicators, new sessions, and impossible travel.
- Train users to verify domains carefully and block known phishing infrastructure.








