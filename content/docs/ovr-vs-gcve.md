---
title: "What Makes OVR Different from GCVE?"
date: 2025-05-02
draft: false
description: "Understand how the OVR Foundation differs from GCVE and CVE initiatives, and why it matters."
tags: ["OVR", "GCVE", "Vulnerability", "Standard", "CVE"]
---

## Introduction

While GCVE (Global CVE) and the OVR Foundation share a commitment to improving how the world identifies and tracks software vulnerabilities, they take very different approaches in scope, governance, and long-term goals.


### Mission and Focus

|                  | **GCVE**                                          | **OVR Foundation**                                                  |
|------------------|---------------------------------------------------|---------------------------------------------------------------------|
| **Purpose**       | Decentralized CVE-compatible vulnerability IDs   | Establish a **new open standard** for global vulnerability tracking |
| **Started by**    | CIRCL (CERT Luxembourg)                          | Independent initiative                                              |
| **Approach**      | Operational, pragmatic (alternative to CVE blocks) | Strategic, governance-first, standard-focused                       |
| **Compatibility** | CVE-compatible (via GNA ID 0)                    | CVE-compatible (via ovr:cve.org:0-2025-1234)                        |
| **Scope**         | Numbering & publishing of vulnerabilities        | Standards, policy, governance, legal, tooling                       |


### Technical Architecture

#### GCVE
- Federated system of **GCVE Numbering Authorities (GNAs)**
- Format: `GCVE-<GNA-ID>-<YEAR>-<ID>`
- No central block allocation

#### OVR
- Not yet bound to a format — aims to define a **consensus-based global format**
- Format: `ovr:<authority>:<product>-<year>-<id>`
- Cryptographically signed and independently verifiable
- Envisions integration with SPDX, OSV, SBOM, and coordinated disclosure workflows
- Emphasizes **trust models, transparency and dispute resolution**


### Governance Philosophy

| Aspect              | **GCVE**                                 | **OVR Foundation**                                                                     |
|---------------------|--------------------------------------------|----------------------------------------------------------------------------------------|
| **Governance**      | None formalized — each GNA is autonomous | Democratic, independent, transparent and accountable governance model planned          |
| **Trust model**     | Based on GNA digital signatures           | Based on cross-organizational consensus and open participation                         |
| **Quality control** | Optional (GNA-defined policies)           | Core part of the standard — includes guidance for disclosure, scoring, and remediation |


### Why OVR?

The OVR Foundation exists because the **centralized dependency on U.S.-based CVE infrastructure** has proven fragile — as seen in recent funding threats to MITRE/CISA. A single point of failure in global security coordination is unacceptable.

**OVR's goals include:**
- Enabling **any country or community** to participate in vulnerability coordination
- Creating a **truly open and sustainable global registry system**
- Supporting **legal and policy frameworks** beyond technical ID formats


### Coexistence, Not Competition

GCVE is a strong step forward in making vulnerability reporting more inclusive and scalable. OVR builds on the same spirit but **reaches beyond identifiers**, proposing a **neutral, legally and politically independent foundation** for the future of global software security.


Want to help shape the future of vulnerability standards?  
- 💬 Join our [Matrix Space](https://matrix.to/#/#ovr-foundation:nope.chat)
- 🐘 Follow us on [Mastodon](https://infosec.exchange/@ovr)
- 🧵 Follow us on [Bluesky](https://bsky.app/profile/ovr-foundation.org)
