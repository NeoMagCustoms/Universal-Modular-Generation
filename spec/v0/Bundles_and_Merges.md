# Bundles and Merges

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

**Bundles** and **Merges** are composition mechanisms used by Universal Modular
Generation (UMG) to combine blocks prior to synthesis.

They define how blocks are grouped or fused, but do not themselves perform
resolution or execution.

---

## Bundles

A **bundle** is a grouping of blocks in which all blocks apply together
**without semantic fusion**.

In a bundle:
- each block retains its original meaning
- no new semantic intent is created
- all bundled blocks remain independently identifiable

Bundles express coexistence, not combination.

---

## Bundle Characteristics

Bundles:
- preserve block identity
- do not alter block semantics
- do not resolve conflicts
- do not suppress blocks

Any conflict between bundled blocks is handled later during synthesis,
using priority and governance rules.

---

## Merges

A **merge** is a composition operation in which two or more blocks combine
to form **new cognitive intent**.

In a merge:
- the resulting intent is not reducible to its inputs
- original blocks contribute to a new semantic whole
- the merge itself is a meaningful operation

Merges explicitly create new meaning.

---

## Merge Characteristics

Merges:
- produce a new block or composite intent
- require explicit declaration
- must be traceable to their source blocks
- do not occur implicitly

A merge never happens by proximity, order, or inference.

---

## Relationship to Synthesis

Bundles and merges define **inputs** to the synthesis process.

They do not:
- resolve conflicts
- determine dominance
- enforce constraints
- produce compiled outputs

Synthesis consumes bundles and merges—along with priority, governance,
and MOLT ordering—to produce RuntimeSpec and Trace.

---

## Determinism

Bundle and merge behavior must be explicitly declared and deterministic.

Given the same blocks and declared bundle/merge operations, a UMG-compliant
system must interpret them identically.

---

## Summary

Bundles express coexistence without semantic change.  
Merges express fusion that creates new intent.

Both are explicit composition mechanisms whose effects are resolved
only during synthesis.
