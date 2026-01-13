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

## Priority, Selection, and OFF

Priority does not disable or exclude blocks.

Priority resolves conflicts **only among elements that are permitted to
participate** in synthesis.

When multiple permitted elements cannot all apply simultaneously, priority
determines which element is selected for that synthesis outcome.

Elements that are not selected:
- remain defined
- remain eligible
- are not set OFF
- may be selected in future synthesis passes

**OFF** is the only mechanism that excludes an element from synthesis.
OFF may be applied only through governance or explicit author intent.

Priority cannot set OFF.
Priority cannot override governance.

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

## Interaction with Governance

Priority is evaluated only after governance constraints are applied.

Priority cannot:
- enable elements excluded by governance
- override governance decisions
- bypass OFF states imposed by governance

When governance excludes an element, priority is not evaluated for that element.

---

## Scope of Application

Priority applies during **synthesis** when:

- bundled blocks conflict
- merged intent competes with existing blocks
- governance rules require selection
- multiple applicable constraints collide

Priority has no effect outside of conflict resolution.

---

## Priority and Repeated Synthesis

Priority resolution applies per synthesis pass.

A selection outcome does not permanently exclude non-selected elements.
Future synthesis passes may select different elements if inputs or constraints change.

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

---

## Clarification Note

In this document, the terms *interaction* and *relationship* are used deliberately
to describe different concerns:

- **Interaction with Governance** refers to *operational sequencing* —  
  what happens when priority and governance are both present during synthesis.

- **Relationship to Governance** refers to *conceptual authority* —  
  which mechanism is allowed to override another, under any circumstances.

Interaction describes **how rules are applied**.  
Relationship describes **which rules are supreme**.

This distinction is intentional and prevents ambiguity between execution order
and authority hierarchy.
