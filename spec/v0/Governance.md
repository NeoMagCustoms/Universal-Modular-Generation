# Governance

> Version: UMG Spec v0  
> Status: Normative

---

## Definition

**Governance** is the authoritative constraint and policy layer within Universal
Modular Generation (UMG).

Governance defines **what is allowed**, **what is forbidden**, and **what must be
present** in a cognitive specification. It bounds synthesis outcomes and prevents
invalid or unsafe configurations.

Governance does not execute behavior.  
Governance constrains synthesis.

---

## Purpose

The purpose of governance is to:

- enforce non-negotiable invariants
- prevent invalid or unsafe compositions
- bound dynamic reconfiguration
- resolve conflicts that cannot be solved by priority alone
- ensure deterministic, auditable outcomes

Governance exists to prevent implicit drift, emergent authority, or uncontrolled
reconfiguration.

---

## Scope

Governance may apply to:

- individual blocks
- NeoBlocks
- NeoStacks
- entire sleeves

Governance constraints are evaluated during synthesis.

Governance does **not**:
- execute logic
- observe runtime behavior
- infer intent
- learn or optimize
- modify block content

---

## Governance and Synthesis

Governance is enforced during synthesis.

Before a block, NeoBlock, or NeoStack may participate in a synthesis outcome,
it must satisfy all applicable governance constraints.

If a governance rule excludes an element, that element is set **OFF** and excluded
from the synthesis scope.

Governance enforcement is deterministic and must be recorded in the Trace.

---

## OFF Semantics

**OFF** is an explicit exclusion state.

An element marked OFF:
- remains defined
- retains identity
- is excluded from synthesis participation

OFF does not delete or modify content.

If multiple governance rules apply, exclusion by governance takes precedence over
inclusion by any other mechanism.

Lower-level rules may not re-enable an element that has been set OFF by a higher-
authority governance constraint.

---

## Governance and Priority

Priority is not governance.

Priority is a deterministic tie-breaker used **within** governance-permitted scope.

Governance determines **what may participate**.  
Priority determines **which permitted elements prevail** when conflicts occur.

If governance forbids an outcome, priority cannot override that decision.

---

## Conditional Governance via TriggerState

Governance rules may reference explicit, declared inputs (TriggerState).

In this model, governance does not toggle elements dynamically at runtime.
Instead, governance is applied during synthesis using the current TriggerState
to determine inclusion or exclusion.

When TriggerState changes, a new synthesis pass may be performed, producing a new
RuntimeSpec and Trace snapshot reflecting updated governance constraints.

---

## Conflict Handling

Governance conflicts must resolve deterministically.

If governance rules produce incompatible outcomes, the implementation must either:
- resolve the conflict using explicit precedence rules, or
- treat the conflict as a synthesis error

Silent conflict resolution is not permitted.

---

## Immutability and Authority

UMG Spec v0 assumes governance rules are authored by a trusted authority.

Governance constraints are authoritative and may not be overridden by ordinary
blocks, merges, or synthesis ordering.

An implementation may treat governance as immutable or privileged, requiring
explicit authorization to modify. Rules for governance mutation are
implementation-defined and out of scope for v0.

---

## Trace Requirements

When governance affects synthesis, the Trace must record:
- the governance rule applied
- the condition matched (including TriggerState if relevant)
- the affected elements
- the resulting action (e.g., OFF, exclusion, enforced inclusion)

This ensures governance effects are inspectable and auditable.

---

## Summary

Governance defines the non-negotiable boundaries of cognition in UMG.

It constrains synthesis deterministically, prevents hidden drift, and enables
dynamic reconfiguration without sacrificing auditability or control.

---

Note: Reference implementations may not fully enforce all governance constraints
defined in this specification.
