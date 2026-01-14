# VALIDEXOR

VALIDEXOR is a deterministic verifier.

It does not decide.
It does not execute.
It does not repair.

It evaluates whether a claim is **verifiable against observable reality**.

---

## Philosophy

VALIDEXOR exists to end ambiguity without creating authority.

It is designed for moments where:

* Claims must be checked, not debated
* Language must be anchored to facts
* Truth depends on falsifiability, not intent

VALIDEXOR does not assert truth.
It asserts whether truth *can be asserted*.

---

## What It Is

VALIDEXOR is a **verification primitive**.

It inspects input and determines whether it satisfies the minimum conditions required for verification.

The result is a verdict about **verifiability**, not correctness.

---

## What It Is Not

* Not a judge
* Not a linter
* Not an executor
* Not an interpreter
* Not an oracle

VALIDEXOR never mutates state.

---

## Behavior

* Consumes input **exclusively** via `stdin`
* Refuses silent invocation
* Rejects speculative or hedged language
* Requires at least one falsifiable anchor
* Validates referenced git objects against repository state
* Emits exactly one verdict
* Exits immediately after evaluation

No retries.
No flags.
No configuration.

---

## Verdicts

VALIDEXOR emits exactly one of the following:

* `VERIFIED` — the claim is concrete and falsifiable
* `UNVERIFIABLE` — the claim lacks sufficient anchors
* `INVALID` — the claim contains speculation or invalid references

The verdict concerns **structure**, not **truth**.

---

## Usage

VALIDEXOR is never run alone.
It must receive a claim.

```sh
<command-producing-claim> | ./validexor.sh
```

### Example

```sh
echo "build output hash is a3f9c21" | ./validexor.sh
```

Output:

```
VERIFIED
```

```sh
echo "this might be correct" | ./validexor.sh
```

Output:

```
INVALID
```

---

## Contract

Once emitted:

* The verdict stands
* Interpretation is external
* Responsibility remains with the claimant

VALIDEXOR guarantees **verifiability**, not **accuracy**.

---

## Design Constraints

These constraints are intentional:

* No configuration → no framing bias
* No execution → no side effects
* No judgment → no authority

Verification precedes meaning.

---

## Relationship to Other Artifacts

* **GUILLOTINE** — executes
* **IRREVOCULL** — judges
* **ATTESTORIUM** — witnesses
* **VALIDEXOR** — verifies

Each artifact performs exactly one irreversible role.

---

## Warning

Verification can invalidate narratives.

That is the point.

---

## About

VALIDEXOR is a minimal, deterministic verifier for claims that must survive contact with reality.

If you want persuasion, do not use it.
If you want verification, nothing else will do.
