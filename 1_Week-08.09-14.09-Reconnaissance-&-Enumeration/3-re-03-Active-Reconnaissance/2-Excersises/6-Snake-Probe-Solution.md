# 🐍 Snake-Probe 

**Course:** Cyber Security Analyst - Active Reconnaissance | **Date:** 10 September 2025

---

## Task

**Goal:**  
Develop a basic TCP port scanner in Python to understand its fundamental operation and compare its capabilities with `nmap`.

**Requirements:**

- Write a Python script (`py_scanner.py`):
    
- It should take a target IP and a comma-separated list of TCP ports as command-line arguments.
    
- For each port, attempt a TCP connection with a timeout.
    
- Print whether each port is "Open" or "Closed".
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

```python
import argparse
import socket


def scan_port(host: str, port: int, timeout: float = 0.5) -> bool:
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as sock:
        sock.settimeout(timeout)
        try:
            return sock.connect_ex((host, port)) == 0
        except OSError:
            return False


def main():
    parser = argparse.ArgumentParser(description="Simple TCP port scanner")
    parser.add_argument("target", help="Target host or IP")
    parser.add_argument("ports", help="Comma-separated TCP ports")
    parser.add_argument("--timeout", type=float, default=0.5, help="Socket timeout in seconds")
    args = parser.parse_args()

    ports = [int(port.strip()) for port in args.ports.split(",") if port.strip()]
    for port in ports:
        state = "Open" if scan_port(args.target, port, args.timeout) else "Closed"
        print(f"{args.target}:{port} -> {state}")


if __name__ == "__main__":
    main()
```

### Comparison with `nmap`

- `nmap` offers service/version detection, OS fingerprinting, NSE scripts, UDP scanning, timing controls, and richer output formats.
- The Python scanner is useful for quick automation, embedding in other scripts, or environments where you only need a tiny, dependency-free TCP connectivity check.

### Example usage

```bash
python py_scanner.py scanme.nmap.org 22,80,443
nmap -sT scanme.nmap.org -p 22,80,443
```








