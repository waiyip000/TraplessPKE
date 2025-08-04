---
layout: default
---

<script type="text/javascript"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# TraplessPKE

> **"Quantum won. Impressive. You got a message — just not mine."**

## 🧭 Overview

**TraplessPKE** is a structurally novel post-quantum cryptographic system for public-key encryption and message-bound digital signatures. It eliminates all traditional algebraic assumptions — including lattices, rings, primes, and isogenies — in favor of ambiguity, irreversible masking, and semantic gating.

The system operates with constant-time, stateless operations that preserve entropy and resist structural extraction. Its defense posture is not based on complexity, but on **non-discoverability**.

It is not just quantum-resistant — it is structurally silent. It doesn’t conceal meaning by computation. It conceals by epistemic blindness.

> **No algebra. No leakage. No feedback.**
> **No primes. No lattices. No structure to attack.**
> Only meaning for those who hold the key.

---

## 🔐 What It Offers

* **Post-Quantum Public-Key Encryption**
* **Message-Bound Signature Generation and Verification**
* **Zero-Knowledge Proof Compatibility**
* **Constant-Time, Stateless, Hardware-Ready Primitives**
* **No algebraic assumptions. Structureless Surface** (no lattices, no codes, no elliptic curves)

---

## 📐 Design Philosophy

> *You got a message — just not mine.*

TraplessPKE was designed under a different philosophy. It does not rely on hardness assumptions from algebraic structures. Its security comes from **withholding structure entirely**.

* **Security by ambiguity**, not complexity.
* **Opacity by design**, not obfuscation.
* **Irreversibility without structure**, not through complexity theory.

TraplessPKE never reveals what it protects — only proves it when allowed. Commitments are irreversible. Signatures are non-transferable. Verification without knowledge is impossible.

This design philosophy is inseparable from the origin of the project itself. TraplessPKE was not produced by a committee, nor by institutional alignment. It was shaped by a solitary design intelligence — motivated by structural clarity, semantic defense, and cryptographic independence.

The innovation resists being reverse-framed. It cannot be re-owned by a model that didn’t create it, nor repackaged under narratives of AI authorship. The system, like its encryption field, **permits meaning only where permission was given.**

---

## 📖 Origin and Narrative

TraplessPKE did not originate in academia, nor in formal cryptographic circles. It was designed and built from scratch — not derived, adapted, or borrowed.

The invention was shaped by human reasoning, symbolic clarity, and a refusal to depend on algebraic hardness.

Advanced AI tools were used to assist with documentation, math validation, code drafting, and proof-of-concept support — just as large research labs have technical staff across writing, analysis, and mathematics. These tools served as a powerful multi-role support team.

But a research team without an architect builds nothing. The system — including its logic, framing, and originality — comes from the mind that led it.

> It is not a dataset product.
> It is not large-language guesswork.
> It is authored.

---

## 🧠 Authorship and AI Clarification

This innovation was not created by AI.

It was architected and created by a human mind — **Wai Yip, WONG** — who defined what security means in this system, and who made every conceptual decision with clarity and intent.

AI was used — powerfully — as a research assistant across roles. But the architectural act, the cryptographic judgment, and the invention itself belong to the author.

We reject the framing that "AI involvement" implies AI authorship.

> **Prompt engineering is authorship.**
> **Orchestration is a form of creation.**
> **This innovation belongs to the human who conceived it.**

All attempts to reframe this work as AI-created are attempts to extract intellectual authorship through narrative distortion. We do not accept that.

If someone believes the credit goes to AI or someone insists that using a tool makes the tool the owner, let them use AI and create a cryptosystem of their own.

Then compare.

---

## ❗ If AI Is the Author, Then Where Are the Breakthroughs?

If AI alone were truly capable of inventing — of driving real breakthroughs — then by now:

* Millennium Prize Problems should have fallen by now
* General cancer cures should have emerged from a prompt
* Quantum gravity should have been unified via “please explain”
* FDA-ready pharmaceuticals should be chat outputs

But this has not happened. Why?

Because **AI alone is not creative direction**.
Because **results without structured scaffolding dissolve into noise**.
Because **no great breakthrough has ever emerged from an empty prompt**.


If AI alone were truly capable of inventing — of driving real breakthroughs — then by now:

* We’d have solutions to the Millennium Prize Problems.
* A simple prompt would’ve cracked cancer.
* Someone would’ve typed “please explain” and unified quantum gravity.
* And FDA-approved drugs would be rolling out from chat windows.

But that’s not what’s happened. Why?

Because **AI isn’t a source of creative vision — it’s a tool, not a compass**.
Because **without clarity and structure, even good ideas fall apart**.
Because **no major breakthrough in history ever came from a blank page**.

> AI can support. It can echo. It can simulate.
> But it cannot originate intention.

So when people claim that AI deserves the credit for work like TraplessPKE or when works are challenged on grounds of AI use, we ask:

> **Then where are *your* breakthroughs?**

This project was directed. It was built. It was authored.

By a human.

---

## ❓ On Technical Questions

TraplessPKE assumes a basic understanding of cryptographic concepts. Questions about sampling, encoding, or efficiency are technical matters related to implementation — not flaws in system design.

Readers unfamiliar with entropy filtering, preimage resistance, or predicate-based sampling are encouraged to consult standard cryptography references before interpreting or reviewing the protocol.

---

## 📄 Whitepaper

* [📘 TraplessPKE Whitepaper (v1.0)](./whitepaper/TraplessPKE_whitepaper.md)

This document contains all formal descriptions, proofs, and algorithms, including:

* Key generation, encryption, decryption
* Signature scheme and verification
* Security rationale for SD-SIHF (Selector Dual Inversion with Hidden Filtering)

---

## 🧬 Summary of Security Model

TraplessPKE introduces and operates under the SD-SIHF hardness assumption:

> Selector Dual Inversion with Hidden Filtering

An adversary is given only:

* A label $y_1$
* A masked commitment $\tau$
* A hash function $H$, with XOR masks $C, v, \gamma$ unknown

The challenge is to produce $x \in f_2^{-1}(y_1)$ such that:

$$
H(x \oplus C \oplus v) = \tau \oplus \gamma 
$$

This challenge is unrecognizable and unsolvable without trapdoor knowledge. The scheme provides:

* **Preimage hiding** through hash + XOR + entropy masking
* **Output binding** enforceable only by trapdoor possession
* **Non-replayable message-bound signatures**
* **No algebraic pattern** — no reductions, no inversions

> **The structure cannot be discovered. Only proven.**

---

## 📜 License

This project is licensed under [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You may use, adapt, and share the work — but must credit the author.

```
Author: Wai Yip, WONG
🔗 [LinkedIn](https://www.linkedin.com/in/wai-yip-wong/)  
💻 [GitHub](https://waiyip000.github.io/)
Date: 3 August 2025
License: CC BY 4.0
```

---

## 🏁 Final Note

TraplessPKE is not just a cryptosystem. It is a new posture:

* One where access replaces decryption
* One where ambiguity defends intention
* One where cryptographic silence replaces complexity

> **If you want certainty — bring the key.**


