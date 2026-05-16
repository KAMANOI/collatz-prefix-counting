# Direct Prefix Counting and Deterministic Synchronization Collapse

**Paper V — Separating Gate Mass from First-Record Prefix Density**

Establishes a critical distinction between gate mass and first-record prefix density, and shows that the prefix density is governed by an exact first-passage probability of a deterministic map — strictly smaller than the naive gate-mass bound.

> This repository does not claim a proof of the Collatz conjecture.

---

## Overview

Gate mass (fraction of gate-1 renewal events at the target residue) and first-record prefix density (fraction of Kᵢ-record orbits achieving Kᵢ₊₁ as their next height record) are conceptually distinct. Numerically, gate mass is approximately 40% while prefix density is approximately 15% — nearly three times smaller. This paper explains the gap exactly.

The central results are:

- **Lemma DSC-pre** (exact): After a Kᵢ-cascade, the odd core satisfies q ≡ 3^{L_{Kᵢ}} r_{Kᵢ} ≢ r_{K_{i+1}} (mod 2^{Kᵢ}) — the starting position is deterministically fixed and does not coincide with the target
- **Theorem 4.1 (FPO)** (First-Passage Obstruction, exact): |S_{i+1}(N)|/|Sᵢ(N)| equals the first-passage probability from a fixed start q_{cascade} to a fixed target r_{K_{i+1}} under gate-1 renewal dynamics — a purely deterministic quantity
- **Conjecture DSC** (Deterministic Synchronization Collapse, numerical): |S_{i+1}|/|Sᵢ| ≤ 2^{−(K_{i+1}−Kᵢ)} with C ≤ C₀ < 1 for all Kᵢ ≥ 4

---

## Main Results

### Proved (Rigorous)

| Result | Method | Status |
|--------|--------|--------|
| Lemma DSC-pre: exact starting position after cascade | Cascade algebra | ✓ proved |
| Theorem FPO: prefix density = first-passage probability | Exact reduction | ✓ proved |
| All measured C < 1 | Numerical | ✓ observed |

### Conjectural

| Conjecture | Evidence | Status |
|------------|----------|--------|
| DSC: C ≤ C₀ < 1 for all Kᵢ ≥ 4 | Numerical (n₀ ≤ 10⁵) | open |

---

## Structure

```
§1   Introduction: the gate mass trap
§2   Gate mass vs first-record prefix density
§3   The starting position after a cascade     ✓ (Lemma DSC-pre)
§4   Numerical evidence for Conjecture DSC
§5   Proof strategy for Conjecture DSC         open
§6   Summary
```

---

## Open Problems

- **Conjecture DSC**: Prove that the first-passage probability from q_{cascade} to r_{K_{i+1}} satisfies FPP ≤ 2^{−(K_{i+1}−Kᵢ)} · C₀ with C₀ < 1 uniformly for Kᵢ ≥ 4

---

## Repository Structure

```
collatz-prefix-counting/
├── README.md
├── paper/
│   └── paper_v_direct_prefix_counting.pdf
└── LICENSE
```

---

## Related Work

This paper is part of a series on Collatz dynamics:

- [collatz-act1](https://github.com/KAMANOI/collatz-act1) — Foundational paper: prime survival dynamics and Chen-type theorem (v11)
- [collatz-renewal-structure](https://github.com/KAMANOI/collatz-renewal-structure) — Paper A: exact operator structure and finite information memory
- [collatz-finite-mixing-geometry](https://github.com/KAMANOI/collatz-finite-mixing-geometry) — Paper B: finite-level mixing geometry
- [collatz-spectral-amplification](https://github.com/KAMANOI/collatz-spectral-amplification) — Paper C: spectral amplification
- [collatz-scale-coherence](https://github.com/KAMANOI/collatz-scale-coherence) — Paper D: scale-coherence rigidity
- [collatz-valuation-renewal](https://github.com/KAMANOI/collatz-valuation-renewal) — Valuation renewal, finite residue connectivity, and orbitwise gap
- [collatz-residual-core](https://github.com/KAMANOI/collatz-residual-core) — The residual core: structural decomposition
- [collatz-congruence-synchronization](https://github.com/KAMANOI/collatz-congruence-synchronization) — Paper H: nested congruence constraints on synchronization
- [collatz-record-renewal](https://github.com/KAMANOI/collatz-record-renewal) — Paper N: record renewal compatibility
- [collatz-hensel-escape](https://github.com/KAMANOI/collatz-hensel-escape) — Paper O: Hensel memory and 2-adic escape target
- [collatz-hensel-scarcity](https://github.com/KAMANOI/collatz-hensel-scarcity) — Paper T: Hensel conditional scarcity and telescoping contradiction
- [collatz-prefix-counting](https://github.com/KAMANOI/collatz-prefix-counting) — Paper V: direct prefix counting and synchronization collapse
- [collatz-first-passage](https://github.com/KAMANOI/collatz-first-passage) — Paper W: first-passage obstruction (closes series A–V)
- [collatz-series-summary](https://github.com/KAMANOI/collatz-series-summary) — Series summary: research program on Collatz synchronization dynamics
- [collatz-prime-survival](https://github.com/KAMANOI/collatz-prime-survival) — Paper X v20: prime survival in affine Collatz dynamics

---

## Author

Hiroki Kamanoi
hirokikamanoi@gmail.com
2026
