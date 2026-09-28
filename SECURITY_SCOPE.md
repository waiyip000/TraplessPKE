# Two-Boundary security scope

Updated 28 September 2026.

## Effects and observer information

Let the candidate files be M0 and M1, and let I be the sender's intended index.

- **Recovery correctness:** the authorized receiver obtains MI from the transmitted bundle and private identity.
- **Content boundary:** what an observer can recover about M0 and M1.
- **Intent boundary:** what an observer can infer about I from the information available to that observer.

Correct recovery is not itself evidence that an observer cannot infer I. Exposing all candidate contents also does not, by itself, identify I. A claim about intent requires the observation and selection conditions to be stated.

## Demonstration views

| View | Disclosed information | What remains outside that view |
|---|---|---|
| V0 | Public identity and bundle | Private identity and owner selection records |
| V1a | V0 plus both actually decoded candidate files | Intent authority and selected-index diagnostics |
| V1b | V1a plus content private-key/decoding authority | Intent private key and owner truth |
| Owner walkthrough | Owner inputs, selected index and actual recovered output | This is an owner functional demonstration, not a blinded experiment |

These are explicit serialized exports. The exporter runs with owner authority; the exports do not simulate arbitrary access to every byte in its process memory. Only disposable demo identities should be used for exposure.

## Dependencies and limits

The demonstration uses separate content and intent capabilities based on ML-KEM-768, together with authenticated encryption and binding. It does not hide a proprietary TraplessPKE algorithm.

Disclosing the content capability while withholding the intent capability is a specific experiment. A general compromise of the common underlying primitive may affect both capabilities; this demo does not establish survival in that condition.

Other excluded or unresolved conditions include:

- Endpoint takeover, arbitrary memory access, operating-system confinement and guaranteed erasure.
- Whole-program constant-time execution and absence of timing or other side channels.
- Intent inference from meaningful candidate differences or external knowledge.
- Independence of peer ordering based solely on owner-controlled local records.
- A universal bound over all observers, messages, environments or algorithms.

For two candidates and a uniformly random hidden index, uninformed guessing succeeds with probability one half. That reference point does not automatically apply to human-selected files with informative side context. No numerical security bound is claimed from the local functional controls.

## Functional evidence versus peer evidence

Local functional acceptance exercises actual operations and failure handling. It supports the tested behavior and exact recorded artifact, not universal unbreakability.

A blinded peer exchange needs a fixed public view, independent prediction submission before reveal, and a recorded accounting of outcomes and abstentions. Owner-authored teaching examples are identified separately. The intended demo publication will include its exact protocol, limitations and sanitized acceptance records.

“Oracleless” here describes the absence of an online owner service that confirms intended-file guesses. Ordinary local decryption, signature verification in the commercial application, and owner comparison still return results; the term does not mean every operation everywhere emits no feedback.

## Intended-route confidentiality and release time

In the proposed [transport use case](USE_CASES.md), the intended index selects a route file. The sender's decision is fixed before bundle finalization. An authorized release time is a separate policy: possession of both the bundle and usable private-key capability already permits recovery. No trusted-clock enforcement or remote revocation is established by the current documented workflows.

Exposing candidate contents can reveal sensitive route information even when the intended index remains uncertain. Common facts across candidates and external knowledge remain informative. More candidates alone do not justify a real-world 1/N inference bound.

Limiting disclosure to designated staff requires access control and key custody outside the serialized exposure experiment. Bundle authenticity and current-instruction freshness are also distinct; signature validity alone does not make an old route instruction current.

## Commercial application

The commercial release has its own implementation and acceptance scope. It includes signature and vault workflows absent from the demo. Research publication, successful owner recovery and finite plan acceptance are distinct facts; none is an IEEE certification of commercial software security.

For reports, see [SECURITY.md](SECURITY.md).
