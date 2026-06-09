# 🐍 Taylor-Made 

**Course:** Cyber Security Analyst - Active Reconnaissance | **Date:** 10 September 2025

---

## Task

**Goal:**  
Develop a custom service and an Nmap Scripting Engine (NSE) script to detect it by its unique banner.

**Requirements:**

- **Create a Custom Server (Python):**
    
- Develop a Python script that listens on a chosen TCP port (e.g., 13337) on `localhost`.
    
- Upon connection, the server should send a unique banner (e.g., `Welcome to MySuperSecretServer v1.0 Alpha!\\r\\n`) and then close the connection.
    
- Run this server.
    
- Output:
    
    - `Submit the final result in the exact format requested by the task.`
        
    - `A reviewer-readable final result`
        
    - `The submission artifact requested by the task`

---

## Solution

### `custom_server.py`

```python
import socket


HOST = "127.0.0.1"
PORT = 13337
BANNER = b"Willkommen bei MySuperSecretServer v1.0 Alpha!\r\n"


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as server:
    server.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)
    server.bind((HOST, PORT))
    server.listen(5)
    print(f"Listening on {HOST}:{PORT}")

    while True:
        client, address = server.accept()
        with client:
            print(f"Connection from {address[0]}:{address[1]}")
            client.sendall(BANNER)
```

### `mysecretserver-detect.nse`

```lua
local nmap = require "nmap"
local shortport = require "shortport"

description = [[Detects the MySuperSecretServer banner on TCP/13337.]]
author = "Codex"
license = "Same as Nmap--See https://nmap.org/book/man-legal.html"
categories = {"safe", "discovery"}

portrule = shortport.portnumber(13337, "tcp")

action = function(host, port)
  local sock = nmap.new_socket()
  sock:set_timeout(2000)

  local ok = sock:connect(host.ip, port.number)
  if not ok then
    return nil
  end

  local status, banner = sock:receive()
  sock:close()

  if status and banner and banner:find("MySuperSecretServer v1.0 Alpha!", 1, true) then
    return "MySuperSecretServer v1.0 Alpha detected on " .. host.ip .. ":" .. port.number
  end
end
```

### Test command

```bash
nmap -Pn -p 13337 --script ./mysecretserver-detect.nse 127.0.0.1
```

Use the terminal screenshot from that run as the submission evidence.








