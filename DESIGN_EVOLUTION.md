# From the original idea to implemented effects

Dated clarification: 28 September 2026. This document accompanies the unchanged 2025 whitepaper; it does not edit that historical artifact.

## Continuity of purpose

The central question is whether access to candidate contents also identifies which candidate the sender intended. Authorized recovery and unauthorized intent inference are different effects.

A useful correspondence must identify the sender's inputs, the recipient's inputs, the observer's information and the resulting output. Sharing a name, slogan or diagram does not establish identical behavior across versions.

## Distinct records

| Record | What it identifies | How to use it |
|---|---|---|
| Whitepaper v1.0, 2025 | Initial selector/mapping/predicate and masked-commitment proposal, called SD-SIHF in that text | Read as the preserved original proposal, including its original claims |
| IEEE CCNC 2026 paper | Published research record under its own title and DOI | Cite the paper; do not assume its exact construction from the earlier PDF |
| Commercial desktop 1.1.4 | Later private implementation and customer workflows | Use its version-specific customer documentation and accepted scope |
| Demo 0.1.2 | Separate inspectable two-candidate construction with content and intent capabilities | Inspect its complete protocol and the exact exported observer views |

The exact IEEE paper text was not available to the documentation reviewer. This refresh therefore does not assert a complete algorithm-by-algorithm equivalence between that paper and the implementations.

## Clarifications to the original whitepaper

The following are document-level reconciliation points, not executable exploit instructions or a claim that current commercial software shares the historical construction.

| Original material | Clarification for present readers |
|---|---|
| Section 3.1 and section 5 explanations | A parameter included in the stated public key is elsewhere discussed as withheld. A current description must give one consistent public/private field classification. |
| Sections 3.2–3.3 | Public candidate selection and private acceptance are described separately without a complete arbitrary-message correctness derivation connecting them. Current functional correctness must be assessed on actual sender and receiver operations. |
| Candidate enumeration and section 8.1 | Enumeration does not itself establish fixed runtime or absence of variable-length loops. Current documents make no whole-implementation constant-time claim. |
| Section 6 performance tables | The original estimates have no accompanying executable measurement artifacts in the historical repository. They are not benchmarks for desktop 1.1.4 or demo 0.1.2. |
| Claims of no algebraic assumptions or universally absent leakage | These do not describe the demo's concrete ML-KEM and authenticated-encryption dependencies. Current claims are scoped to actual capabilities and observations. |
| Signature, zero-knowledge and platform-readiness descriptions | A conceptual capability is not automatically an implemented feature. The demo omits signatures and zero-knowledge integration; commercial functionality is listed separately. |

The historical README also described some public parameters differently from the original PDF. The preserved historical files retain that discrepancy; current documentation uses the explicit capability description in [SECURITY_SCOPE.md](SECURITY_SCOPE.md).

## Current functional account

For the demo, the sender supplies two candidate files and one intended index. Both contents are carried in a bundle. Separately protected intent information lets an authorized recipient select the intended output. The owner walkthrough compares actual recovered bytes with the original selection.

The inspection workflow can expose both decoded candidates and content authority while withholding intent authority. This defines a narrower observation than a full memory compromise. Content and intent use separate generated capabilities but share the ML-KEM primitive.

Thus content exposure and a general break of that primitive are different experimental conditions. The former does not establish survival of the latter. Sender side information, candidate plausibility and endpoint observations must also be included when making an intent-inference claim.

The commercial implementation's accepted work is retained under its own scope. No demo result automatically validates the entire commercial system, and no commercial milestone retroactively proves every historical whitepaper assertion.

## Application mapping: intended transit route

The proposed [protected-transport use case](USE_CASES.md) gives the content/intent distinction a business interpretation: approved route files are candidates, and the sender chooses the route to execute. Unselected candidates can be genuine alternatives.

The mapping introduces a separate time condition: selected staff should learn the choice only at authorized release. That condition does not follow merely from the candidate/selector construction. Existing recovery works whenever the recipient has both the bundle and usable private-key access. Selection occurs before bundle finalization; a later route change requires a new bundle and a process for superseding earlier instructions.

This application proposal preserves the original idea while distinguishing file-level implemented effects from additional dispatch-system requirements. It is not evidence of deployment or a new security result.

## Inspect the implemented demonstration

Use the demo's [protocol](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/PROTOCOL.md), [observation model](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/THREAT_MODEL.md), [walkthrough](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/WALKTHROUGH.md) and [peer-exchange instructions](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/PEER_EXCHANGE.md) for implementation-specific details. [Functional validation](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/VALIDATION.md) identifies the tested 0.1.2 artifact; it does not establish equivalence with every historical proposal.

---

[Research home](README.md) · [Repository guide](PROJECT_MAP.md) · [Demo source](https://github.com/waiyip000/traplesspke-two-boundary-demo) · [Demo manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/USER_MANUAL.md)
