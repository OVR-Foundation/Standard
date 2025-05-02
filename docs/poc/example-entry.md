---
id: poc-example-entry
title: Example Disclosure
sidebar_label: Example Disclosure
description: Example of a PoC entry format including SBOM reference.
---

# Example Disclosure Entry

This is an example of how a security disclosure could be published and verified under the OVR model, including an optional SBOM reference.

```yaml
id: "openvuln:example.com:firefox-2025-0001"
title: "Firefox allows access to saved passwords without master password"
description: >
  A vulnerability in Firefox's password manager allows local attackers
  to extract stored credentials if no master password is set.


technical_details: >
  The internal storage for saved passwords is not encrypted by default.
  If a user does not manually configure a master password, saved credentials
  are accessible through the local profile storage without needing authentication.
  An attacker with local filesystem access can retrieve the file
  `logins.json` and decrypt stored data using known static keys.

affected:
  - product: "Mozilla Firefox"
    versions:
      - "< 124.0.1"
    platform: "Windows, Linux, macOS"

impact:
  severity: HIGH
  vector: LOCAL
  cvss: 6.8

discovery:
  reported_by: "security@example.com"
  published: "2025-04-18"

identity:
  authority: "example.com"
  did: "did:openvuln:dns:example.com"
  public_key: |
    -----BEGIN PUBLIC KEY-----
    MFYwEAYHKoZIzj0CAQYFK4EEAAoDQgAEwK...
    -----END PUBLIC KEY-----
  dns_verification:
    txt_record: "_openvuln.example.com"
    expected_value: "pubkey=MFYwEAYHKo..."
    dnssec: true
    verified_at: "2025-04-18T14:00:00Z"

signature:
  algorithm: "ecdsa-secp256r1"
  signature_value: "MEUCID8xQnFu32B4m...cZ9=="

metadata:
  license: "CC0-1.0"
  format_version: "0.1"

sbom:
  reference_url: "https://example.com/sbom/firefox-2025-0001.json"
  integrity_hash: "sha256:b1946ac92492d2347c6235b4d2611184"

```


| Field            | Description                                                | Required |
|------------------|------------------------------------------------------------|----------|
| id               | Unique identifier for the vulnerability report.            | ✅       |
| title            | Short, human-readable title of the vulnerability.          | ✅       |
| description      | Brief description of the vulnerability in plain language.  | ✅       |
| technical_details| Detailed technical explanation of the vulnerability.        |        |
| affected         | List of affected products, versions, and platforms.        | ✅       |
| impact           | Severity, attack vector, and CVSS score of the vulnerability. | ✅    |
| discovery        | Information about who reported the issue and when.         | ✅       |
| identity         | Cryptographic identity information about the organization. | ✅       |
| signature        | Digital signature to verify authenticity of the report.    | ✅       |
| metadata         | License and format version information.                    | ✅       |
| sbom             | Reference to a Software Bill of Materials (SBOM).         |        | affected product. | 🔲