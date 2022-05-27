# SBOM Software Bill of Materials

- [SBOM Software Bill of Materials](#sbom-software-bill-of-materials)
  - [Quick Start (Mac)](#quick-start-mac)
    - [Prerequisite](#prerequisite)
  - [Research](#research)
    - [NTIA](#ntia)
      - [Introduction to SBOM](#introduction-to-sbom)
      - [Understanding SBOM](#understanding-sbom)
      - [SBOM Implementation](#sbom-implementation)
      - [Technical Resources](#technical-resources)
      - [Lessons from the Proof of Concept Work](#lessons-from-the-proof-of-concept-work)
      - [Other Resources](#other-resources)
    - [CISA](#cisa)
      - [Events](#events)
      - [Resources](#resources)
      - [More information](#more-information)
    - [K8S SBOM](#k8s-sbom)
    - [K8s Admission Control Using SBOMs](#k8s-admission-control-using-sboms)
    - [Image Scanner](#image-scanner)
    - [Formats](#formats)
    - [Generating SBOMs](#generating-sboms)
    - [Related Tools](#related-tools)

## Quick Start (Mac)

### Prerequisite

Docker installed

```bash
brew install kind
kind create cluster
```

[https://kind.sigs.k8s.io](https://kind.sigs.k8s.io)

## Research

### NTIA

[https://www.ntia.gov/SBOM](https://www.ntia.gov/SBOM)

A “Software Bill of Materials” (SBOM) is a nested inventory for software, a list of ingredients that make up software components. The following documents were drafted by stakeholders in an open and transparent process to address transparency around software components, and were approved by a consensus of participating stakeholders. More information about the NTIA multistakeholder process on software component transparency is available [here](/SoftwareTransparency).

#### Introduction to SBOM

- [SBOM at a Glance (2021)](https://ntia.gov/files/ntia/publications/sbom_at_a_glance_apr2021.pdf)  
This resource provides an introduction to the practice of SBOM, supporting literature, and the pivotal role SBOMs play in providing much-needed transparency for the software supply chain.  ([Japanese translation](https://ntia.gov/files/ntia/publications/sbom_at_a_glance_ja.pdf))

- [SBOM FAQ (2021)](https://ntia.gov/files/ntia/publications/sbom_faq_-_20201116.pdf)  
This document outlines detailed information, benefits, and commonly asked questions.

- [SBOM Myths vs. Facts (2021)](https://ntia.gov/files/ntia/publications/sbom_myths_vs_facts_nov2021.pdf)
This document is intended to help the reader to understand and dispel common, often sincere myths and misconceptions about SBOM.

- [SBOM Explainer Videos on YouTube (2020-2021) (link is external)](https://youtube.com/playlist?list=PLO2lqCK7WyTDpVmcHsy6R2HWftFkUp6zG)  
This collection of videos provides a wide range of information about SBOM including introductory concepts, technical webinars, and proof of concept presentations.

<details>
<summary>NTIA Continued ... CLICK to expand</summary>

#### Understanding SBOM

- [Framing Software Component Transparency: Establishing a Common Software Bill of Materials (SBOM) – (2021)](https://ntia.gov/files/ntia/publications/ntia_sbom_framing_2nd_edition_20211021.pdf)  
This resource serves as the detailed foundation of SBOM. It defines SBOM concepts and related terms, offers an updated baseline of how software components are to be represented, and discusses the processes around SBOM creation. (prior [2019 edition](https://ntia.gov/files/ntia/publications/framingsbom_20191112.pdf))

- **[SBOM Options and Decision Points (2021)](https://ntia.gov/files/ntia/publications/sbom_options_and_decision_points_20210427-1.pdf)**  
This resource frames the dimensions of SBOM creation and delivery, to support more consistent and effective articulation of needs between requesters and suppliers of SBOMs.  

- **[Use Cases: Roles and Benefits for SBOM Across the Supply Chain (2019)](https://ntia.gov/files/ntia/publications/ntia_sbom_use_cases_roles_benefits-nov2019.pdf)**  
This resource summarizes the use cases and benefits of having an SBOM from the perspective of those who make software, those who choose or buy software, and those who operate it. It characterizes the security, quality, efficiency, and other organizational benefits, as well as the potential for the broader ecosystem across the supply chain.

- [**SBOM Tool Classification Taxonomy (2021)**](https://ntia.gov/files/ntia/publications/ntia_sbom_tooling_taxonomy-2021mar30.pdf)  
This resource offers a categorization of different types of SBOM tools. It can help tool creators and vendors to easily classify their work, and can help those who need SBOM tools understand what is available.

#### SBOM Implementation

- [**Survey of Existing SBOM Formats and Standards (2021)**](https://ntia.gov/files/ntia/publications/sbom_formats_survey-version-2021.pdf)  
This resource summarizes existing standards, formats, and initiatives as they apply to identifying the external components and shared libraries used in the construction of software products for SBOMs, highlighting three key formats of SPDX, CycloneDX, and SWID. The group analyzed efforts already underway by other groups related to communicating this information in a machine-readable manner. (prior [2019 edition](/ntia/publications/ntia_sbom_formats_and_standards_whitepaper_-_version_20191025.pdf))

- [Software Suppliers Playbook: SBOM Production and Provision (2021)](https://ntia.gov/files/ntia/publications/software_suppliers_sbom_production_and_provision_-_final.pdf)  
This resource outlines workflows for the production of Software Bills of Materials (SBOM) and their provision by software suppliers, including software vendors supplying a commercial product, contract software developers supplying a software deliverable to clients, and open source software (OSS) development projects making their capabilities publicly available.

- [Software Consumers Playbook: SBOM Acquisition, Management, and Use (2021)](https://ntia.gov/files/ntia/publications/software_consumers_sbom_acquisition_management_and_use_-_final.pdf)  
This resource outlines workflows for the acquisition, management, and use of SBOM by software consumers, including commercial and non-commercial entities acquiring third-party software capabilities from a supplier.

- [How-To Guide for SBOM Generation (2021)](https://ntia.gov/files/ntia/publications/howto_guide_for_sbom_generation_v1.pdf)  
This resource offers instructions and guidance on how to generate an SBOM based on the experiences of the Healthcare Proof-of-Concept working group.

- [Sharing and Exchanging SBOMs (2021)](https://ntia.gov/files/ntia/publications/ntia_sbom_sharing_exchanging_sboms-10feb2021.pdf)
This resource describes how SBOM data can flow down the supply chain, and provides a small set of SBOM discovery and access options to support flexibility while minimizing the burden of implementation.

#### Technical Resources

- [**Software Identity: Challenges and Guidance (2021)**](https://ntia.gov/files/ntia/publications/ntia_sbom_software_identity-2021mar30.pdf)  
This resource reviews the challenges of identifying software components for SBOM implementation with sufficient discoverability and uniqueness. It offers guidance to functionally identify software components in the short term and converge multiple existing identification systems in the near future.

- [**SBOM Tool Classification Taxonomy (2021)**](https://ntia.gov/files/ntia/publications/ntia_sbom_tooling_taxonomy-2021mar30.pdf)  
This resource offers a categorization of different types of SBOM tools. It can help tool creators and vendors to easily classify their work, and can help those who need SBOM tools understand what is available.

- [Vulnerability-Exploitability eXchange (VEX) - An Overview (2021)](https://ntia.gov/files/ntia/publications/vex_one-page_summary.pdf)  
This resource offers a brief introduction to VEX, which allows a software supplier to clarify whether a specific vulnerability actually affects a product.

#### Lessons from the Proof of Concept Work

- [How-To Guide for SBOM Generation in Healthcare (2021)](https://ntia.gov/files/ntia/publications/howto_guide_for_sbom_generation_v1.pdf)  
This resource offers instructions and guidance on how to generate an SBOM based on the experiences of the Healthcare Proof-of-Concept working group.

- [Healthcare SBOM Proof of Concept – Phase II Summary (2021)](https://ntia.gov/files/ntia/publications/healthcare_sbom_proof_of_concept_-_phase_ii_summary.pdf)  
Phase II confirmed the value of providing SBOM information, proving the viability of the baseline elements, expanding use cases and participants, developing a how-to guide, and exploring the use of VEX.

- **[Healthcare Proof of Concept Report (2019)](https://ntia.gov/files/ntia/publications/ntia_sbom_healthcare_poc_report_2019_1001.pdf)**  
This resource documents the successful execution and lessons learned of a proof-of-concept exercise led by medical device manufacturers (MDMs) and healthcare delivery organizations (HDOs). The exercise examined the feasibility of SBOMs being generated by MDMs and used by HDOs as part of operational and risk management approaches to medical devices at their hospitals.

#### Other Resources

- [Software Bill of Materials Related Efforts (2021)](https://ntia.gov/files/ntia/publications/sbom_related_efforts_oct2021.pdf)  
A collection of initiatives, guidance, models, frameworks, and reports that explicitly or implicitly highlight the value of SBOM.

- [**Software Identity: Challenges and Guidance (2021)**](https://ntia.gov/files/ntia/publications/ntia_sbom_software_identity-2021mar30.pdf)

This resource reviews the challenges of identifying software components for SBOM implementation with sufficient discoverability and uniqueness. It offers guidance to functionally identify software components in the short term and converge multiple existing identification systems in the near future.

- [SBOM Two-Page Overview (2020)](https://ntia.gov/files/ntia/publications/sbom_overview_20200818.pdf)  
This document provides high-level information on SBOM’s background and ecosystem-wide solution, the NTIA process, and an example of an SBOM.

**For more information, please contact [mdoscher@ntia.gov](mailto:mdoscher@ntia.gov)**

**For upcoming and archived meeting details, please visit the [NTIA Software Component Transparency page](/SoftwareTransparency).**
</details>

### CISA

[https://www.cisa.gov/sbom](https://www.cisa.gov/sbom)

A “software bill of materials” (SBOM) has emerged as a key building block in software security and software supply chain risk management. A SBOM is a nested inventory, a list of ingredients that make up software components.  The SBOM work has advanced since 2018 as a collaborative community effort, driven by [NTIA’s multistakeholder process](http://ntia.gov/SBOM).

CISA will advance the SBOM work by facilitating community engagement, development, and progress, with a focus on scaling and operationalization, as well as tools, new technologies, and new use cases. This website will also be a nexus for the broader set of SBOM resources across the digital ecosystem and around the world.

An SBOM-related concept is the [Vulnerability Exploitability eXchange (VEX).](https://ntia.gov/files/ntia/publications/vex_one-page_summary.pdf)  A VEX document is an attestation, a form of a security advisory that indicates whether a product or products are affected by a known vulnerability or vulnerabilities. For more information on how to receive updates or join in on the efforts around VEX, please contact [SBOM@cisa.dhs.gov(link sends email)](mailto:SBOM@cisa.dhs.gov).

<details>
    <summary>CISA continued ... CLICK to expand</summary>
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

### K8s Admission Control Using SBOMs

#### Available Tools

- [Ratify](https://github.com/deislabs/ratify) - Integrates with OPA Gatekeeper to verify the authenticity/provenance of artifacts and their supplied attestations (including SBOMs)
- [Cosigned Admissions Controller](https://docs.sigstore.dev/cosign/kubernetes/#cosigned-admission-controller) - Uses cosign/sigstore to verify metadata of container images before admitting them in a cluster. This *can* include the authenticity/provenance of an SBOM.
- [OPA - Conftest](https://github.com/open-policy-agent/conftest) - Allows writing OPA/rego tests for application configuration. Includes native module for parsing CycloneDX and SPDX SBOM material. This *should* allow creating rules based on the contents of an SBOM (example: presence of a vulnerable version of log4j in the dependency tree).

### Formats

SPDX is an open standard for communicating software bill of material information, including provenance, license, security, and other related information. SPDX reduces redundant work by providing common formats for organizations and communities to share important data, thereby streamlining and improving compliance, security, and dependability. The SPDX specification is recognized as the international open standard for security, license compliance, and other software supply chain artifacts as ISO/IEC 5962:2021.
[https://spdx.dev/about/](https://spdx.dev/about/)

CycloneDX

### Generating SBOMs

#### Available Tools

- [Syft](https://github.com/anchore/syft) - By Anchore. Supports CycloneDX and SPDX Formats. Can create in-toto spec compatible SBOM attestations.
- [Tern](https://github.com/tern-tools/tern) - Supports CycloneDX and SPDX Formats. SBOMs generated layer by layer for container images.

### Related Tools

- [in-toto](https://github.com/in-toto/in-toto) - Specification and toolset for tracing and validating supply chain integrity. Does not generate SBOMs, but can be used to sign and validate them
- [witness](https://github.com/testifysec/witness) - Implementation of in-toto specification with some additional bells and whistles. Roadmap includes using CACs for signing/attestation of images and implementing a K8s Admissions Controller.
- [grype](https://github.com/anchore/grype) - Vulnerability scanner by Anchore, works seamlessly with Syft to scan for vulnerabilities based on SBOM data. Not an admissions controller, but could potentially be used to provide data to one about vulnerability status of an image.
