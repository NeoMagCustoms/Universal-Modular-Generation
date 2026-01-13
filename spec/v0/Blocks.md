# Blocks

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

A **block** is the atomic unit of meaning in Universal Modular Generation (UMG).

Blocks represent discrete cognitive contributions—such as goals, rules,
constraints, instructions, heuristics, or abstract ideas—that may be composed
into larger cognitive structure.

Blocks carry **semantic intent** but do not encode execution behavior.

---

## Purpose

The purpose of blocks is to:

- provide modular units of cognitive meaning
- allow cognition to be composed incrementally
- preserve traceability of individual contributions
- enable explicit control over how meaning is combined

Blocks make cognition explicit and inspectable.

---

## Structure

Every block must define:

- an identifier
- a semantic payload (content)
- a MOLT role

Additional metadata may be present, but must not alter the block’s semantic intent
or structural interpretation.

---

## Blocks and MOLT

Each block is associated with a **MOLT role** that determines how it participates
in structural composition.

The MOLT role governs:
- how the block relates to other blocks
- how it is ordered and contextualized
- how it is treated during synthesis

A block without a MOLT role is invalid.

---

## Identity and Persistence

Blocks retain their identity throughout composition.

Even when blocks are bundled, merged, or synthesized:
- the original blocks remain identifiable
- their participation must be traceable
- suppression or dominance must be explicitly recorded

Blocks are never implicitly modified or erased.

---

## Semantic Neutrality of Structure

Blocks do not derive meaning from:
- their position
- neighboring blocks
- ordering outcomes
- synthesis results

Meaning is authored, not inferred.

Structural interpretation is handled exclusively by MOLT and synthesis rules.

---

## Relationship to Composition

Blocks may participate in:

- **bundles**, where multiple blocks coexist without semantic fusion
- **merges**, where blocks combine to form new cognitive intent
- **synthesis**, where composed structures are resolved into compiled form

These processes do not alter the definition of a block itself.

---

## Summary

Blocks are the **semantic atoms** of UMG.

They encapsulate discrete meaning while remaining structurally neutral,
allowing cognition to be generated through explicit, deterministic composition.
