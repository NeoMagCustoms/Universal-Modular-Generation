# Trace

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

**Trace** is the authoritative forensic record produced by synthesis in
Universal Modular Generation (UMG).

Trace documents **how** a synthesis outcome was derived, including structural
decisions, exclusions, selections, and transformations applied during
compilation.

Trace does not execute behavior.  
Trace records resolution.

---

## Purpose

The purpose of Trace is to provide:

- auditability of cognitive structure
- reproducibility of synthesis outcomes
- transparency of governance and priority effects
- inspection of dynamic reconfiguration
- prevention of silent drift or hidden inference

Trace ensures that no synthesis outcome exists without an explicit explanation.

---

## Scope

Trace records **structural resolution only**.

Trace may include:

- governance exclusions and routing decisions
- OFF assignments
- bundle evaluation order
- merge operations and resulting composites
- priority-based selections
- resulting active structures

Trace does **not** include:

- execution behavior
- runtime actions
- model outputs
- learned state or optimization
- interpretation of semantic content

---

## Trace Generation

A Trace is generated for **every synthesis pass**.

Each Trace corresponds to a single compilation snapshot and reflects the inputs
and decisions applied during that pass.

Repeated synthesis (e.g., hotswap or state updates) produces **multiple Trace
snapshots**, each independently auditable.

---

## Required Trace Elements

A UMG-compliant Trace must record, at minimum:

- synthesis pass identifier
- referenced specification version
- applied governance rules and outcomes
- elements excluded via OFF
- bundle and merge operations applied
- priority assignments and selections
- resulting active structural elements

Trace entries must be explicit and deterministic.

---

## Governance and Trace

All governance effects must be recorded in Trace.

This includes:
- exclusions
- routing decisions
- priority assignments
- enforced invariants

Governance effects may not occur silently.

---

## Priority and Selection in Trace

When priority-based selection occurs, Trace must record:

- the competing elements
- their priority values
- the selection outcome
- the reason selection was required

Non-selected elements remain defined and may appear in future synthesis passes.

---

## Trace Immutability

Trace records are immutable once produced.

A Trace represents a historical account of synthesis and must not be altered
retroactively.

Subsequent synthesis passes produce new Trace records rather than modifying
existing ones.

---

## Relationship to RuntimeSpec

Trace and RuntimeSpec are complementary outputs of synthesis.

- **RuntimeSpec** describes *what is active*
- **Trace** describes *how that state was reached*

Neither output replaces the other.

---

## Determinism

Given identical synthesis inputs, a UMG-compliant system must produce an identical
Trace.

Non-deterministic Trace output is not permitted.

---

## Implementation Status (Non-Normative)

Not all Trace elements defined in this specification may be fully populated by
current reference tooling.

Partial Trace output does not invalidate the specification.

Reference implementations may expand Trace fidelity over time.

---

## Summary

Trace is the audit backbone of Universal Modular Generation.

It ensures that cognitive structure is transparent, explainable, and resistant
to silent modification, enabling responsible use of dynamic and modular cognitive
systems.
