# Current project status

Status date: 28 September 2026.

## Commercial Windows application

**Release 2 / Windows desktop 1.1.4** is the current commercial production baseline, owned by Wai Yip, WONG. The baseline was assigned to existing accepted bytes; it is not a new executable version.

Supported customer workflows include:

- Create reusable protected keys and export public keys.
- Register keys in a backup vault.
- Encrypt files and decrypt a bundle.
- Sign a bundle and verify a signature.
- Back up and restore a vault.
- Change a key password and resume a saved job.

The “Encrypt and validate” workflow separately displays the intended full path and performs actual encryption, decryption and byte-for-byte comparison with the selected original. This owner validation workflow needs the matching recipient private key and password. It is distinct from public-key-only sending to another recipient.

Resource admission is automatic. Recovery folders may retain plaintext and must remain private. The current user interface is Windows-only; Linux interface work and macOS are paused.

The underlying revised V2.2 plan records 34/34 criteria accepted within the retained finite scopes. Desktop 1.1.4 has retained change-specific validation. Neither statement extends to every environment, every observer or arbitrary endpoint compromise. CPU/iGPU utilization targets are not claimed achieved.

The source, internal construction tools, private evidence and private baseline archives are not included in this repository. Customer distribution uses a separately licensed source-free package; this page is not a download, purchase or support commitment.

## Open-source demonstration

**Demo 0.1.2** is a separate two-candidate Python implementation. It includes public-key sending, private-key recovery, owner byte comparison, explicit candidate/content-capability exposure, and commitment/submission/reveal exchange.

Local package construction and sequential functional acceptance completed successfully, with actual acceptance exit 0. The public release provides source, a standalone Windows x64 executable, the offline Python kit and user manual. Published asset downloads matched their recorded SHA-256 hashes, and the downloaded executable actually recovered the selected file with equal bytes. These are functional and distribution checks, not a security proof.

[Dedicated demo repository](https://github.com/waiyip000/traplesspke-two-boundary-demo) · [Release downloads](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2) · [User manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/USER_MANUAL.md). Demo source licence: Apache-2.0, with dependency-specific notices. Commercial source is excluded.

The demo omits the commercial GUI, signature workflows, vault and commercial internals. It uses ML-KEM-768 and AES-256-GCM-SIV. Its published algorithm is intended to be fully inspectable, without a hidden commercial backend. No independent blinded security bound has been established.

## Proposed transport application

Cash-in-transit, valuables-in-transit and VIP-in-transit route confidentiality is the author's proposed priority business use case. Candidate route plans map to candidate files, and the chosen route maps to the intended file. Protected-transport companies can evaluate TraplessPKE for integration into their operational workflows, based on their business needs, confidentiality requirements and deployment conditions. See [USE_CASES.md](USE_CASES.md).

This documentation adds no product capability. Current workflows select the intended file before finalizing the bundle. Timed release, staff authorization, current-instruction tracking and dispatch integration are not established by existing file-level acceptance. The demo remains limited to two candidates; no transport-themed run or operational deployment is claimed.

## Publication review

This documentation refresh is under owner review with the repository temporarily private. Making it public again requires completion of that review. Original commits, the whitepaper PDF and release V1.0 remain preserved.

See [SECURITY_SCOPE.md](SECURITY_SCOPE.md), [LICENSING.md](LICENSING.md) and [HISTORY.md](HISTORY.md).

## Latest demonstration validation

On 28 September 2026 the expanded sequential Windows suite completed: all 14 CLI commands, all six core workflow families, both optional iGPU example producers and observed execution of 57/57 named application functions. It recorded 80 terminal invocations and 81 core-worker invocations. Two local harness defects were repaired; no demo application change was required. See the demo's [dated result and limits](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/VALIDATION.md).

Documentation on the main branches is maintained separately from the immutable demo v0.1.2 release assets. The [repository guide](PROJECT_MAP.md) identifies each repository's role and access conditions.

---

[Research home](README.md) · [Repository guide](PROJECT_MAP.md) · [Demo source](https://github.com/waiyip000/traplesspke-two-boundary-demo) · [Demo manual](https://github.com/waiyip000/traplesspke-two-boundary-demo/blob/main/USER_MANUAL.md)
