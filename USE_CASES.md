# Intended-route confidentiality for protected transport

Proposed priority business use case identified by Wai Yip, WONG on 28 September 2026: **cash-in-transit, valuables-in-transit and VIP-in-transit operations**.

This scenario applies where an operator prepares several approved route plans, chooses one for a particular movement and limits disclosure of that choice until an authorized operational release. It is a use-case proposal, not a claim of customer deployment or a measured ranking against other markets.

## Mapping the business operation to TraplessPKE

| Business object or role | TraplessPKE correspondence |
|---|---|
| Approved alternative route plans | Candidate message files |
| Dispatcher or authorized decision-maker | Sender |
| Route selected for this movement | Intended file |
| Collection of candidate files with protected selection information | Bundle |
| Authorized recipient | Holder of the applicable private-key access |
| Operational release decision | Separate delivery/access-control policy |
| Recipient's recovered instruction | Selected route file |

The unselected routes can be genuine alternatives that were considered but not chosen. “Decoy” describes their role relative to the selected route; it need not mean an impossible or fabricated route.

For N candidates, let the route files be R0 through R(N−1) and let I be the sender's chosen index. The authorized recovery objective is to recover RI. The intent-confidentiality question is whether an observer can identify I from that observer's available information.

The current inspectable demo has exactly two candidates. This business mapping does not remove implementation limits or add an arbitrary-route-count capability.

## Operational sequence and release timing

1. The operator prepares and approves the candidate route files in its private planning environment.
2. The authorized sender makes the final route choice and identifies the corresponding intended file.
3. The sender constructs a bundle for the applicable recipient and, where supported and required, uses the commercial signing workflow for authenticity.
4. The operator releases access to the usable bundle to the designated recipient at the authorized time.
5. The recipient recovers the selected file. An owner validation workflow can separately compare actual recovered bytes against the selected original.

The sender chooses the intended file **before finalizing the bundle** in the current documented workflows. The choice may be made late, but construction, validation and delivery still take time. No maximum end-to-end dispatch latency is established here.

An existing finalized bundle is not a remotely changeable route instruction. A different choice requires a newly constructed bundle and an operational process that identifies the current instruction and supersedes the old one. Previously disclosed information cannot be recalled by changing a file or issuing a replacement bundle.

## “Last-minute” is an access condition

Let B be the bundle, K the usable private-key capability and t_release the authorized release time. A person who already holds both B and K can run recovery before t_release. The current documented recovery operation does not consult a trusted release clock.

Therefore the required pre-release condition is operational: before t_release, the recipient must not have access to both B and usable K. One possible arrangement is to keep recipient private keys under the recipients' control and withhold delivery of the bundle until release. Another would require a separately engineered key-access control system. Neither is an intrinsic timer in TraplessPKE.

This proposal does not establish scheduled key release, remote revocation, quorum approval, a dispatch server or managed multi-recipient access in the existing application. Limiting disclosure to selected people requires recipient authorization and key custody; a private key does not by itself identify a person's business role.

The commercial “Encrypt and validate” owner workflow needs the matching recipient private key and password. It must not be described as a public-key-only dispatch workflow or used as a reason to give recipient private keys to unauthorized planning staff. The demo's separate sender path uses only the public identity. Actual organizational integration must respect those distinct workflows.

## The two boundaries in this scenario

**Content boundary:** protects the contents of the route plans from observers outside the stated access conditions.

**Intent boundary:** concerns which route among the candidates was selected. The demo's explicit content-exposure view reveals both candidate files while withholding intent authority. That is the condition in which intended-index inference is studied.

A candidate-content exposure is still a disclosure of route information, even if the selected index is unknown. Candidate files can share sensitive locations, times or other common facts. Hiding I does not hide a fact present in every candidate.

Route plausibility and outside information can also influence inference. Increasing the number of candidates does not automatically provide a 1/N real-world success bound, and human route selection is not assumed uniform. No guarantee that an observer cannot infer the route follows solely from placing alternatives in a bundle.

## Existing capabilities and integration work

| Requirement | Status in this proposal |
|---|---|
| Explicit intended-file selection and private-key recovery | Existing documented file workflows |
| Owner round-trip byte comparison | Existing commercial validation and demo owner walkthrough |
| Signature generation/verification | Commercial functionality; absent from the current demo |
| Two-candidate inspectable exposure scenario | Current demo scope |
| Timed release and authorized staff access | Organizational/integration responsibility; not established as built-in features |
| Current-instruction tracking, expiry and replay handling | Dispatch integration requirement; a valid signature alone does not establish freshness |
| Operator deployment, release latency and operational effectiveness | Not established by existing local functional acceptance |

Recovery folders, copies and planning files remain within the operator's confidentiality obligations. Learning the selected route through an authorized recipient or compromised endpoint is outside the demo's narrower exported view.

## Demonstration material and publication

Any future transport-themed public example should use clearly fictional route files and disposable identities. Public documentation should contain no actual journeys, operational schedules, client locations, VIP identities or reusable credentials.

This document adds the business mapping only. It does not claim a route-themed demonstration has already been executed, change the commercial baseline, publish the demo or disclose private implementation details.

See [current status](CURRENT_STATUS.md), [design evolution](DESIGN_EVOLUTION.md) and [security scope](SECURITY_SCOPE.md).
