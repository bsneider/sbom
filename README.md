# SBOM Software Bill of Materials

- [SBOM Software Bill of Materials](#sbom-software-bill-of-materials)
  - [Quick Start (Mac)](#quick-start-mac)
    - [Prerequisite](#prerequisite)
  - [Research](#research)
    - [CISA](#cisa)
      - [Events](#events)
      - [Resources](#resources)
      - [More information](#more-information)
    - [K8S SBOM](#k8s-sbom)
    - [Image Scanner](#image-scanner)
    - [Formats](#formats)

## Quick Start (Mac)

### Prerequisite

Docker installed

```bash
brew install kind
kind create cluster
```

[https://kind.sigs.k8s.io](https://kind.sigs.k8s.io)

## Research

[https://www.ntia.gov/SBOM](https://www.ntia.gov/SBOM)

### CISA

[https://www.cisa.gov/sbom](https://www.cisa.gov/sbom)

A “software bill of materials” (SBOM) has emerged as a key building block in software security and software supply chain risk management. A SBOM is a nested inventory, a list of ingredients that make up software components.  The SBOM work has advanced since 2018 as a collaborative community effort, driven by [NTIA’s multistakeholder process](http://ntia.gov/SBOM).

CISA will advance the SBOM work by facilitating community engagement, development, and progress, with a focus on scaling and operationalization, as well as tools, new technologies, and new use cases. This website will also be a nexus for the broader set of SBOM resources across the digital ecosystem and around the world.

An SBOM-related concept is the [Vulnerability Exploitability eXchange (VEX).](https://ntia.gov/files/ntia/publications/vex_one-page_summary.pdf)  A VEX document is an attestation, a form of a security advisory that indicates whether a product or products are affected by a known vulnerability or vulnerabilities. For more information on how to receive updates or join in on the efforts around VEX, please contact [SBOM@cisa.dhs.gov(link sends email)](mailto:SBOM@cisa.dhs.gov).

<details>
    <summary>CISA Expanded</summary>
#### Events

For a recap of the CISA SBOM-a-rama, held on December 15 & 16, 2021, and to view the recordings of the event, please visit the [CISA SBOM-a-rama page](/cisa-sbom-rama).

#### Resources

For information about the “NTIA Consensus” defining and implementing SBOM, drafted by stakeholders, see the resources at [ntia.gov/sbom](https://ntia.gov/SBOM).

The “Minimum Elements” defined under [Executive Order 14028](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/) are available [at the NTIA SBOM Publications page.](https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf)

[Vulnerability Exploitability eXchange (VEX) Use Case Document (April 2022)](https://cisa.gov/sites/default/files/publications/VEX_Use_Cases_Apr22.pdf)
This resource provides the recommended minimum data elements of a VEX document and offers a set of scenarios with proposed implementations. This document was drafted by stakeholders through an open and transparent, community-led process.

#### More information

For any questions or to receive updates on CISA’s SBOM work, please contact [SBOM@cisa.dhs.gov(link sends email)](mailto:SBOM@cisa.dhs.gov).
</details>

### K8S SBOM

[https://github.com/kubernetes-sigs/bom](https://github.com/kubernetes-sigs/bom)

### Image Scanner

[https://github.com/anchore/syft](https://github.com/anchore/syft)

### Formats

SPDX is an open standard for communicating software bill of material information, including provenance, license, security, and other related information. SPDX reduces redundant work by providing common formats for organizations and communities to share important data, thereby streamlining and improving compliance, security, and dependability. The SPDX specification is recognized as the international open standard for security, license compliance, and other software supply chain artifacts as ISO/IEC 5962:2021.
[https://spdx.dev/about/](https://spdx.dev/about/)
