# VALIDEXOR

Primitive ID: PRIM-005  
Package: @verifrax/validexor  
Binary: validexor

Verifrax primitive — verification primitive for deterministic irreversible systems.

---

## Status

Current release status: pre-stable primitive release line.

Canonical release target:

package version: 0.1.0  
tag: v0.1.0

VALIDEXOR is part of the Verifrax primitive layer and follows the canonical primitive governance, naming, version, and packaging rules.

---

## Purpose

VALIDEXOR verifies deterministic correctness after origin, custody, time, and boundary conditions have already been fixed.

Once an artifact has a stable origin, preserved custody, explicit time boundary, and enforced operating boundary, the system still needs deterministic verification of whether the artifact satisfies the relevant contract. VALIDEXOR exists to make that verification explicit, repeatable, and non-ambiguous.

It does not establish origin. It does not preserve custody. It does not fix temporal order. It does not enforce boundary conditions. It does not witness, judge, or terminate. Its role is narrower: verify contract-level correctness under already-fixed prior conditions.

---

## What This Primitive Does

- verifies an artifact or state against deterministic validation rules
- distinguishes valid from invalid outcomes under a fixed contract
- emits verification output suitable for downstream attestation and judgment

---

## What This Primitive Does Not Do

- does not establish first origin
- does not preserve custody continuity
- does not fix temporal ordering
- does not enforce operational boundaries
- does not witness or attest
- does not judge validity
- does not terminate lifecycle

---

## Behavioral Contract

Invocation model:

executable: validexor  
package: @verifrax/validexor  
runtime: CLI-first

The primitive operates on an artifact whose origin, custody, time, and boundary surfaces are already fixed.

If the verification contract is absent, ambiguous, or non-deterministic, VALIDEXOR must not fabricate a valid result.

Exit codes:

0 — verification completed successfully  
non-zero — invocation failed or contract violated

---

## Usage

Install:

npm install -g @verifrax/validexor

Execute:

validexor artifact.json

stdin example:

cat artifact.json | validexor

---

## Determinism Guarantees

For identical canonical input, VALIDEXOR must produce identical verification output.

No hidden environmental state may influence the result.

VALIDEXOR assumes an already-bounded origin, custody, time, and enforcement surface and does not substitute for those earlier primitives or for downstream attestation and judgment.

---

## Security Model

VALIDEXOR protects against ambiguity in contract verification.

Its security value is to prevent silent drift between what is claimed to satisfy a contract and what deterministically does satisfy it. It does not itself attest, judge, or terminate lifecycle state.

---

## Relationship to Other Primitives

Canonical primitive order:

1 originseal  
2 archicustos  
3 kairoclasp  
4 limenward  
5 validexor  
6 attestorium  
7 irrevocull  
8 guillotine

Repositories:

https://github.com/Verifrax/originseal  
https://github.com/Verifrax/archicustos  
https://github.com/Verifrax/kairoclasp  
https://github.com/Verifrax/limenward  
https://github.com/Verifrax/validexor  
https://github.com/Verifrax/attestorium  
https://github.com/Verifrax/irrevocull  
https://github.com/Verifrax/guillotine

---

## Installation

npm install -g @verifrax/validexor

command -v validexor

Repository:
- GitHub: https://github.com/Verifrax/validexor
- Package: @verifrax/validexor
- Binary: validexor

---

## License

MIT
