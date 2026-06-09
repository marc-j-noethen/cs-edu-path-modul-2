# Service Enumeration

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic focuses on service enumeration: collecting deeper details from already discovered services such as web servers, SMB shares, FTP endpoints, or TLS-enabled applications.

### 2. Key ideas
- Enumeration begins after a host and an open port have already been identified.
- The goal is to learn versions, configurations, exposed content, authentication requirements, and obvious weaknesses.
- Web enumeration often looks at directories, headers, virtual hosts, and certificates.
- Network services such as SMB, FTP, or SSH can reveal useful security-relevant metadata when they are misconfigured.

### 3. Tools and practical relevance
- Nmap can help with service detection and safe metadata collection.
- Gobuster is commonly used in labs to discover hidden web content such as directories or files.
- Curl and browser tools help inspect HTTP headers and manual responses.
- SMB clients can be used in authorized environments to inspect available shares and permissions.

### 4. Key takeaway
Enumeration is where generic network findings become actionable technical understanding.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Nmap | Identify services and collect basic metadata |
| Gobuster | Discover hidden directories or files on web servers |
| curl | Inspect HTTP responses and headers |
| smbclient | Review SMB shares and access behavior in approved labs |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Enumeration | Detailed information gathering from a known service |
| Banner | Text or metadata that identifies a service |
| Virtual host | Multiple websites served from the same web server |
| Directory brute forcing | Testing common paths to discover hidden content |
| SMB | File-sharing protocol commonly used in Windows environments |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| share | network-accessible folder or resource |
| header | metadata in a protocol request or response |
| endpoint | reachable service location |
| certificate | digital identity document used in TLS |
| misconfiguration | insecure or incorrect setup |
