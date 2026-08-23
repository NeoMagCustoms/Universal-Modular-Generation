# UMG Current Canon

**Status:** CURRENT CANON ENTRYPOINT  
**Compiler authority:** UMG compiler-vNext v0.1.0-experimental  
**H4-qualified commit:** `c505f9a7f23010574733c8c03c4162af5317a5eb`  
**H4-qualified tag:** `compiler-vnext-v0.1.0-experimental-h4-qualified`  
**Compiler repository:** `https://github.com/NeoMagnetar/umg-compiler-vnext`

## Authority rule

For current UMG Sleeve compilation, compiler-vNext is the semantic authority.

Applications, runtimes, MCP servers, agents, Studios, Websites, and libraries must conform to the compiler contract. They do not redefine compiler semantics.

## Current object hierarchy

`MOLT Block -> NeoBlock -> NeoStack -> Sleeve`

## Current seven MOLT lanes

1. Trigger
2. Directive
3. Instruction
4. Subject
5. Primary
6. Philosophy
7. Blueprint

Persona and Language are not additional compiler lanes.

## Compiler boundary

The caller/controller supplies explicit Selection state, including active NeoStacks, active NeoBlocks, Trigger truth, supported overlays, Governance selections, and disabled selections.

The compiler validates and resolves that authored structure deterministically and emits RuntimeSpec, Trace, diagnostics, and runtimeHash.

The compiler does not interpret natural-language intent, call a model, invent Trigger state, invent Selection, or execute RuntimeSpec.

## State precedence

`OFF > DISABLED > ACTIVE > READY`

- READY = available
- ACTIVE = participating
- DISABLED = human/configuration exclusion
- OFF = Governance prohibition

## Core semantic distinctions

- **Governance:** explicit OFF-only hard prohibition in v0.1.
- **Bundle:** same-MOLT-type geometry/configuration.
- **Overlay:** temporary additive scoped cognition.
- **Merge:** explicit semantic composition with provenance and authority non-escalation.
- **RuntimeSpec:** executor-facing compiler output.
- **Trace:** compiler derivation/forensic evidence; not execution authority.
- **RuntimeEvents:** execution-time events and not Compiler Trace.

## Legacy warning

The historical `NeoMagCustoms/umg-compiler` / compiler-v0 line is retired for new UMG work.

The existing `/spec/v0` directory in this repository predates the H4 compiler-vNext freeze and is retained for historical/provenance purposes. It must not be used as the current compiler-vNext authority where it conflicts with this canon or the H4-qualified compiler contracts.

## Current documentation

- `docs/current/COMPILER.md`
- `docs/current/SLEEVE_AUTHORING.md`
- `docs/current/RUNTIME_BOUNDARIES.md`
- `docs/current/LIBRARY_PROVENANCE.md`
- `docs/current/LEGACY_MIGRATION.md`

