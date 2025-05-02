---
title: "Architecture"
description: "The conceptual structure of the OVR Proof of Concept and its components."
weight: 30
---

## Introduction

The PoC architecture outlines how different components of the Open Vulnerability Record (OVR) framework work together in a decentralized and verifiable way.


## Identity & Trust

- Each issuer uses a combination of **DID** (Decentralized Identifier) and **DNS** to prove control over a domain.
- DNS TXT records are used to publish the public key fingerprint.
- Optionally, DNSSEC strengthens trust in domain-bound identities.


## SBOM Integration

- Each record can optionally include or reference a **Software Bill of Materials** (SBOM) in SPDX or CycloneDX.
- This enables direct traceability between vulnerability and software components.


## Verification Flow

1. **Fetch OVR Record**
2. **Verify Signature**
3. **Check DNS TXT Record for Public Key**
4. **Match DID and Domain**
5. **Trust Decision via DNSSEC or Web-of-Trust**

---

This architecture is designed for **extensibility**, **transparency**, and alignment with **open standards** like SBOM, CVSS, and Verifiable Credentials.

