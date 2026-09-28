# TraplessPKE

**Created and directed by Wai Yip, WONG.** Updated 28 September 2026.

[廣東話](README_Cantonese.md) · [Publications](PUBLICATIONS.md) · [History](HISTORY.md) · [Current status](CURRENT_STATUS.md)

TraplessPKE explores a distinction between obtaining candidate message contents and identifying the sender's intended message. The sender chooses an intended file among candidate files; the authorized recipient uses private-key material to recover the selected file. The Two-Boundary account separates content access from intent identification and asks what an observer can infer under an explicitly defined exposure.

This repository is the research and project information hub. It preserves the original public record and documents subsequent development.

**Start here:** [Repository guide](PROJECT_MAP.md) · [Demo source](https://github.com/waiyip000/traplesspke-two-boundary-demo) · [Executable and release downloads](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2) · [User manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/USER_MANUAL.md).

Both this research repository and the separate demo repository are public. The demo and its downloads remain self-contained.

## Proposed priority use case: protected transport

Cash-in-transit, valuables-in-transit and VIP-in-transit operations are the author's proposed priority application scenario. Where an operator prepares several approved routes, each route plan becomes a candidate file; the sender's final route choice becomes the intended file. Authorized recipients recover that selection using private-key access.

This maps route alternatives to the distinction between content access and intent identification. Last-minute disclosure also requires controlled delivery or key access: a person who already has the bundle and a usable private key can decrypt it. Selection precedes bundle finalization; this is not a built-in timer or remote route-switching feature.

Protected-transport companies can evaluate TraplessPKE for integration into their operational workflows, based on their business needs, confidentiality requirements and deployment conditions.

[Explore the intended-route workflow and deployment considerations](USE_CASES.md).

## Research publication

Wai Yip Wong, **“TraplessPKE: A Selector-Based, Oracleless, Post-Quantum Cryptosystem,”** 2026 IEEE 23rd Consumer Communications & Networking Conference (CCNC), pp. 1–2.

[IEEE Xplore](https://ieeexplore.ieee.org/document/11366456) · [DOI: 10.1109/CCNC65079.2026.11366456](https://doi.org/10.1109/CCNC65079.2026.11366456) · [Citation and BibTeX](PUBLICATIONS.md)

The [original whitepaper v1.0](TraplessPKE_whitepaper_V1.0.pdf), dated 3 August 2025, remains unchanged as a historical document. It is distinct from the IEEE paper and the later executable implementations. See [design evolution](DESIGN_EVOLUTION.md).

## Current implementations

| Subject | Status and scope |
|---|---|
| Commercial Windows application | Release 2 baseline / desktop **1.1.4**, assigned 28 September 2026. Provides key management, encryption/decryption, signing/verification, backup/restoration and job recovery. The commercial source and internal construction materials remain private. |
| Two-Boundary demonstration | Separate inspectable Python implementation **0.1.2**. Two candidate files, public-key sending, private-key recovery, actual byte comparison and explicit content-exposure views. Demo source, Windows executable and user manual are [available for download](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2). |
| Original whitepaper release | GitHub tag **V1.0**, published 4 August 2025. This identifies the whitepaper release, not commercial application version 1.0.0 or the current desktop release. |

The demonstration is published in its [dedicated repository](https://github.com/waiyip000/traplesspke-two-boundary-demo) under Apache-2.0. [Download the source, executable and user manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2). This repository contains no commercial source or commercial executable download.

## What the demonstration can show

1. A sender explicitly selects one of two candidate files.
2. Sending uses a public identity; receiving uses a private identity.
3. A local owner walkthrough compares the actual recovered bytes with the selected original.
4. A separate inspection workflow exposes both decoded candidates and the content capability while withholding the intent capability.
5. Blinded peer exchange separates prediction submission from the later committed reveal.

The demo uses independently generated content and intent key capabilities, both based on ML-KEM-768. Exposing the content capability is a specific exposure condition; it is not a demonstration of survival after a general break of ML-KEM affecting both capabilities. Local functional results are not an independently established security bound.

Read [security scope](SECURITY_SCOPE.md) for the observer's information, permitted conclusions, and limitations. Candidate plausibility and external context matter to intent inference. No universal unbreakability or whole-process confinement claim is made by these current implementation documents.

## Navigate the project

- [Development chronology and original timestamps](HISTORY.md)
- [Publications and attribution](PUBLICATIONS.md)
- [Current commercial and demonstration status](CURRENT_STATUS.md)
- [Original design and subsequent construction](DESIGN_EVOLUTION.md)
- [Security scope and evidence boundaries](SECURITY_SCOPE.md)
- [Authorship and tool assistance](Author_Clarification.md)
- [Licensing and source separation](LICENSING.md)
- [Reporting issues](SECURITY.md)
- [Documentation changes](CHANGELOG.md)

## Attribution and licensing

The original idea and project direction are attributed to **Wai Yip, WONG**. AI tools assisted research, implementation and documentation under the author's direction.

Research and documentation in this repository are under [CC BY 4.0](LICENSE), unless individually noted. The separate demo source uses Apache-2.0 with its own dependency notices. The commercial implementation is separately licensed and is not included here. The IEEE-hosted article is governed by its applicable publication terms. [Full scope](LICENSING.md).

## Latest demo check

Demo 0.1.2 has [completed Windows functional validation](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/VALIDATION.md): all 14 commands, six core workflow families, both GPU example producers and 57/57 named application functions exercised. The result is scoped to the recorded Windows cases. No application update was required.

---

[Research home](README.md) · [Repository guide](PROJECT_MAP.md) · [Demo source](https://github.com/waiyip000/traplesspke-two-boundary-demo) · [Demo manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/USER_MANUAL.md)
