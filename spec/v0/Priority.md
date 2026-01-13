# Priority

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

**Priority** is a declared ordering used by Universal Modular Generation (UMG)
to resolve conflicts between competing blocks or composed structures during
synthesis.

Priority determines **which contribution prevails** when multiple applicable
elements cannot simultaneously apply.

---

## Purpose

The purpose of priority is to:

- provide deterministic conflict resolution
- prevent implicit or inferred dominance
- preserve authorial control over outcomes
- ensure reproducible synthesis results

Priority exists solely to resolve conflicts.

---

## Declarative Nature

Priority is **explicitly assigned**.

It is not:
- calculated
- inferred
- learned
- optimized
- derived from content
- derived from position
- derived from outcomes

If priority is not declared, no implicit priority exists.

---

## Scope of Application

Priority applies during **synthesis** when:

- bundled blocks conflict
- merged intent competes with existing blocks
- governance rules require selection
- multiple applicable constraints collide

Priority has no effect outside of conflict resolution.

---

## Priority and Meaning

Priority does **not** alter the meaning of a block.

A block with lower priority:
- does not become less meaningful
- does not change semantics
- is not invalidated as an authored contribution

Priority affects **application**, not **definition**.

---

## Determinism

Priority resolution must be deterministic.

Given the same inputs and declared priority assignments, a UMG-compliant
system must always produce the same resolution outcome.

---

## Relationship to Governance

Priority resolves conflicts **within** allowed bounds.

Governance may:
- constrain which priorities are allowed
- override priority assignments explicitly
- disable blocks regardless of priority

Governance is authoritative over priority.

---

## Summary

Priority is a deterministic, declarative mechanism for resolving conflicts
during synthesis.

It does not encode meaning, intent, or value—only resolution order.
