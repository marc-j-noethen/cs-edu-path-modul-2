# MitM and Cryptographic Attacks

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic introduces man-in-the-middle risks and common ways cryptographic protections can fail when validation, trust, or protocol design are weak.

### 2. Key ideas
- A man-in-the-middle attack inserts an attacker between two communicating parties.
- Weak certificate validation, insecure key exchange assumptions, downgrade opportunities, and replayable workflows can all increase risk.
- Cryptography often fails because of implementation or trust mistakes rather than because the underlying math is broken.
- Strong validation, protocol hardening, secure defaults, and user awareness reduce exposure.

### 3. Tools and practical relevance
- Packet analysis tools help defenders understand where trust breaks or unexpected traffic appears.
- Browser warnings and certificate inspection are practical first-line defenses for users and analysts.

### 4. Key takeaway
Secure cryptography depends on secure implementation, secure validation, and secure operational choices.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Wireshark | Review packet-level behavior in controlled lab traffic |
| Browser security indicators | Surface certificate and TLS validation problems to users |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Man-in-the-middle | Interception or relaying of traffic between two parties |
| Downgrade attack | Forcing weaker protocol or algorithm choices |
| Replay attack | Reusing previously valid data or messages |
| Certificate validation | Checking trust chain, hostname, validity, and related properties |
| Trust model | Assumptions about who is allowed to vouch for identity |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| intercept | capture or relay traffic between parties |
| validate | check whether a security property is actually satisfied |
| downgrade | move to a weaker security option |
| replay | send valid old data again |
| trust | confidence placed in an identity or authority |
