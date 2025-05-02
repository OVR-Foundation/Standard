---
title: "Understanding OVR-ID"
description: "Detailed explanation of a sample OVR vulnerability ID and its structure."
weight: 20
---

## Understanding OVR-ID: `ovr:<authority>:<product>-<year>-<id>`

OVR-IDs are structured, verifiable identifiers for software vulnerabilities. Here's the generic format:

### Generic Format

`ovr:<authority>:<product>-<year>-<id>`

| Component            | Value         | Explanation                                                                 |
|----------------------|---------------|-----------------------------------------------------------------------------|
| **Prefix**           | `ovr:`        | Denotes the OVR namespace                                                  |
| **Authority**        | `<authority>` | The domain (or DID) asserting responsibility for the record                |
| **Product Tag**      | `<product>`   | Human-readable project/product identifier                                  |
| **Year**             | `<year>`      | The year the issue was reported or published                               |
| **Serial Number**    | `<id>`        | A sequential number unique per authority and product/year                  |

### Example: `ovr:example.com:app-2025-0001`

This ID refers to the **first published vulnerability of "app" in 2025**, reported by `example.com`.


## CVE Compatibility

OVR-IDs are backward-compatible with CVE identifiers using the following format:

`ovr:cve.org:0-<year>-<id>`

| Component            | Value         | Explanation                                                                 |
|----------------------|---------------|-----------------------------------------------------------------------------|
| **Prefix**           | `ovr:`        | Denotes the OVR namespace                                                  |
| **Authority**        | `cve.org`     | Indicates compatibility with CVE                                           |
| **Reserved Tag**     | `0`           | Reserved for CVE compatibility                                             |
| **Year**             | `<year>`      | The year the CVE was assigned                                              |
| **Serial Number**    | `<id>`        | The CVE ID's unique number                                                 |

### Example: `ovr:cve.org:0-2025-1234`

This ID corresponds to the CVE `CVE-2025-1234` and ensures compatibility with existing CVE systems.
## Purpose

The ID serves as a **globally unique identifier** that:

- Encodes provenance (`example.com`)
- Prevents central registry dependency
- Enables decentralized publication and validation
- Aligns with existing DNS and DID trust systems


## Example Use

This ID can be used to:

- Retrieve vulnerability metadata from Ceramic/IPFS
- Reference the issue in SBOMs or patch notices
- Validate integrity and authorship using DNSSEC and digital signatures


## Validation and Resolution

To verify the authority of the ID:

- Check the DNS TXT record for `_ovr.example.com`
- Validate the associated public key and DID
- Confirm the signature block using the `signature` field in the record


## Related Fields

The full record includes metadata such as:

- Affected software versions
- Severity level (e.g. HIGH, LOCAL)
- Discovery date and author
- Licensing and publication method
- Optional Ceramic or IPFS references
