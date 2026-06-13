# Certificates and TLS

## Summary Based on the 80/20 Principle

### 1. What this topic is about
This topic explains how certificates, public key infrastructure, and TLS work together to protect web traffic.

### 2. Key ideas
- A certificate binds a public key to an identity such as a domain name.
- TLS protects data in transit by providing confidentiality, integrity, and server authentication.
- Browsers validate certificate chains, hostname matching, validity periods, and trust anchors.
- Most real-world TLS deployments use hybrid cryptography: asymmetric methods for setup and symmetric encryption for the session.

### 3. Tools and practical relevance
- Browser certificate viewers help inspect trust chains and certificate metadata.
- OpenSSL helps inspect certificates and test TLS services.
- Wireshark helps visualize handshakes and encrypted traffic patterns in lab environments.

### 4. Key takeaway
TLS is not just "encryption on a website." It is a trust and transport system that depends on correct certificate validation.

---

## Table 1: Tools Used

| Tool | Purpose |
|---|---|
| Browser certificate viewer | Inspect certificate details and trust chain information |
| OpenSSL | Test TLS services and inspect certificate files |
| Wireshark | Analyze handshake behavior and network traces in labs |

## Table 2: Technical Terms

| Term | Meaning |
|---|---|
| Certificate | Digital document that binds a public key to an identity |
| PKI | Public key infrastructure used to issue and trust certificates |
| TLS | Protocol that secures data in transit |
| Certificate chain | Ordered trust path from end-entity certificate to trusted root |
| Perfect forward secrecy | Property that limits the impact of long-term key compromise on past sessions |

## Table 3: Key Vocabulary

| Term | Meaning |
|---|---|
| trust anchor | root certificate trusted by the client |
| handshake | setup phase of a secure connection |
| hostname | domain name being validated |
| issuer | authority that signs a certificate |
| expiry | end of a certificate's validity period |
