# Synthesis

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

**Synthesis** is the deterministic resolution process by which a Universal Modular
Generation (UMG) specification is compiled into an explicit structural outcome.

Synthesis evaluates declared structure, ordering, and constraints to produce a
resolved configuration describing what is active and how it is composed.

Synthesis does not execute behavior.  
Synthesis produces structure.

---

## Purpose

The purpose of synthesis is to:

- resolve authored intent into explicit, inspectable structure
- apply MOLT ordering and structural roles
- enforce governance constraints and OFF semantics
- resolve conflicts deterministically using priority where permitted
- support controlled reconfiguration through repeated compilation

Synthesis ensures cognition is **explicitly resolved**, not inferred.

---

## Inputs

Synthesis operates only on declared inputs:

- the authored UMG specification (blocks, stacks, sleeves)
- bundle and merge operations
- MOLT roles and ordering
- priority assignments (including governance-assigned priority)
- governance rules
- explicit state inputs (TriggerState), if present

Implicit inputs are not permitted.

---

## Governance Enforcement

Governance is enforced during synthesis.

Before any element may participate in synthesis, it must satisfy all applicable
governance constraints.

Elements excluded by governance are set **OFF** and removed from synthesis scope.

Governance decisions are authoritative and cannot be overridden by:
- MOLT ordering
- bundle order
- priority
- selection outcomes
- merge behavior

All governance effects must be recorded in the Trace.

---

## OFF Semantics

OFF is an explicit exclusion state.

Elements marked OFF:
- remain defined
- retain identity
- are excluded from synthesis participation

OFF does not delete or modify content.

Elements set OFF by governance cannot be re-enabled by lower-level mechanisms or
selection outcomes.

---

## MOLT and Structural Precedence

MOLT defines the structural grammar used during synthesis.

MOLT determines:
- how different kinds of blocks contextualize or constrain others
- cross-type precedence relationships
- how structure is interpreted

MOLT does not:
- exclude elements
- disable participation
- infer meaning
- resolve conflicts

MOLT enables structural legibility and hotswap by making composition rules explicit.

---

## Bundles and Merges

Synthesis treats bundles and merges distinctly.

### Bundles

**Bundles** group elements into an ordered structural context without semantic
fusion.

Bundled elements:
- remain independently identifiable
- do not derive new meaning from bundling
- do not gain authority by position alone

Bundle order defines **structural evaluation order** among peers within the same
context.

Bundle order affects *when* elements are considered, not *what* they mean nor
*whether* they are permitted to apply.

---

### Merges

**Merges** produce new composite structures according to explicit merge rules.

Merge outcomes:
- must be deterministic
- must be traceable to their source elements
- are subject to governance, priority, and OFF semantics like any other element

Merges do not bypass governance or structural rules.

---

## Priority and Selection

Priority is applied only within governance-permitted scope.

When multiple permitted elements conflict and cannot all apply simultaneously,
synthesis **selects** outcomes according to declared priority order.

Selection:
- reflects the outcome of a synthesis pass
- does not disable non-selected elements
- does not alter eligibility for future synthesis passes

Priority cannot set OFF.  
Priority cannot override governance.

---

## Recompile Snapshots and Hotswap

Synthesis may be invoked repeatedly over the same specification.

When explicit inputs change—such as TriggerState updates or applied operations
(bundle, merge, routing)—synthesis may be re-run to produce a new resolved outcome.

Each synthesis pass produces:
- a RuntimeSpec
- a corresponding Trace snapshot

This enables **hotswap of cognitive structure** through controlled reconfiguration,
without embedding execution behavior into the specification.

---

## Determinism

Synthesis must be deterministic.

Given identical inputs, a UMG-compliant system must produce identical synthesis
outcomes.

Non-deterministic resolution is not permitted.

---

## Trace Requirements

Synthesis must emit a Trace recording:

- applied bundle and merge operations
- governance exclusions and routing decisions
- priority assignments and selections
- resulting active structures

The Trace provides a complete forensic record of how the synthesis outcome was
derived.

---

## Output

The output of synthesis is a compiled structural description suitable for
consumption by an external system.

This output is expressed as a RuntimeSpec.

UMG does not define how the RuntimeSpec is executed.

---

## Summary

Synthesis is the resolution engine of UMG.

It deterministically composes authored intent into explicit structure, enforces
governance boundaries, resolves conflicts through priority and selection, and
supports dynamic reconfiguration while preserving auditability and alignment.

--

## Implementation Status (Non-Normative)

This document defines the normative semantics of synthesis in UMG.

Not all behaviors described here are fully implemented in the current
reference compiler or UMG Studio.

The reference implementation may support a subset of these semantics.
Absence of an implementation does not invalidate the specification.

Implementation progress is tracked separately from the specification.
