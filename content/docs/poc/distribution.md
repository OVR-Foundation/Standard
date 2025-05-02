---
title: "Ceramic Network Integration"
description: "How the OVR Foundation uses Ceramic Network for decentralized, verifiable, and updatable vulnerability records."
weight: 40
---

## Introduction

The OVR Foundation aims to build a decentralized, resilient, and community-driven vulnerability reporting infrastructure. **Ceramic Network** enables us to store and distribute vulnerability records in a decentralized, tamper-evident, and verifiable way.

Ceramic provides:

- **Immutable but updateable documents** for versioned records
- **Stream anchoring** for integrity and historical tracking
- **DID support** for publisher identity
- **Interoperability** with IPFS and other decentralized tech

## Why Ceramic?

Using Ceramic Network, we can:

- Bind OVR records to a decentralized identity (DID)
- Allow transparent, permissionless updates with audit trails
- Preserve availability using IPFS-based anchoring
- Minimize trust assumptions in the publication process

[//]: # ()
[//]: # (## Example Structure)

[//]: # ()
[//]: # (Below is how Ceramic-specific metadata could be added to an OVR entry:)

[//]: # ()
[//]: # (```yaml)

[//]: # (metadata:)

[//]: # (  license: "CC0-1.0")

[//]: # (  format_version: "0.1")

[//]: # (  ceramic:)

[//]: # (    stream_id: "kjzl6cwe1jw1472vuvix5r9brr0a1a1a1a9i3z90hdpmtq6i2ja4k9e0e5k5zsk")

[//]: # (    url: "https://ceramic-clay.3boxlabs.com/api/v0/streams/kjzl6cwe1jw1472...")

[//]: # (    published_at: "2025-04-20T15:00:00Z")

[//]: # (```)

[//]: # ()
[//]: # (---)

[//]: # ()
[//]: # (## Field Reference)

[//]: # ()
[//]: # (| Field           | Required | Description                                                                 |)

[//]: # (|----------------|----------|------------------------------------------------------------------------------|)

[//]: # (| `stream_id`    | ✅       | Unique ID of the Ceramic stream &#40;used to retrieve the full document&#41;        |)

[//]: # (| `url`          | ❌       | Optional full URL to the stream &#40;for convenience or gateway access&#41;          |)

[//]: # (| `published_at` | ❌       | Optional timestamp when this stream was first published                      |)

[//]: # ()
[//]: # (---)

## Benefits for the Ecosystem

- **Decentralization**: No single point of failure
- **Transparency**: Community-verifiable record histories
- **Extensibility**: Attach SBOMs, patches, and more as updates
- **Governance**: Data remains publicly accessible even as maintainers evolve


[//]: # (## Related Pages)

[//]: # ()
[//]: # (- [OpenVuln Specification]&#40;/specification/&#41;)

[//]: # (- [Identity & DNS Verification]&#40;/specification/identity/&#41;)

[//]: # (- [Decentralized Storage]&#40;/specification/storage/&#41;)
