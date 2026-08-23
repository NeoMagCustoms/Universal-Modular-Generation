# Universal Modular Generation (UMG)

**Universal Modular Generation — Modular Cognitive Architecture for AI Systems.**

UMG is a technology-agnostic architecture for authoring modular cognitive structures, compiling them deterministically, and connecting the resulting runtime contracts to models, agents, tools, applications, and external systems.

## Current canon

Start here:

- [`CANON.md`](CANON.md) — current UMG canon entrypoint
- [`docs/current/COMPILER.md`](docs/current/COMPILER.md) — current compiler authority
- [`docs/current/SLEEVE_AUTHORING.md`](docs/current/SLEEVE_AUTHORING.md) — current Sleeve authoring contract
- [`docs/current/RUNTIME_BOUNDARIES.md`](docs/current/RUNTIME_BOUNDARIES.md) — compiler/runtime/execution boundaries
- [`docs/current/LIBRARY_PROVENANCE.md`](docs/current/LIBRARY_PROVENANCE.md) — Block, component, Sleeve, and experimental library rules
- [`docs/current/LEGACY_MIGRATION.md`](docs/current/LEGACY_MIGRATION.md) — compiler-v0 / legacy migration guidance

## Current compiler authority

Current UMG Sleeve compilation is defined by **compiler-vNext v0.1.0-experimental**.

- Repository: `https://github.com/NeoMagnetar/umg-compiler-vnext`
- H4-qualified commit: `c505f9a7f23010574733c8c03c4162af5317a5eb`
- H4-qualified tag: `compiler-vnext-v0.1.0-experimental-h4-qualified`
- Status: H4 QUALIFIED / FROZEN

The historical `NeoMagCustoms/umg-compiler` / compiler-v0 line is retired for new UMG work.

## Current semantic outline

```text
MOLT Block
    ↓
NeoBlock
    ↓
NeoStack
    ↓
Sleeve
```

Current compiler-vNext uses seven MOLT lanes:

1. Trigger
2. Directive
3. Instruction
4. Subject
5. Primary
6. Philosophy
7. Blueprint

Persona and Language are not additional compiler lanes.

The caller/controller supplies explicit Selection state. The compiler validates and resolves deterministically and emits RuntimeSpec, Trace, diagnostics, and runtimeHash. The compiler does not infer natural-language intent or execute models/tools.

## Historical material

This repository contains earlier UMG specification and documentation material, including `/spec/v0`.

That material is retained for provenance and historical research. It predates the H4 compiler-vNext freeze and must not be treated as current compiler-vNext authority where it conflicts with [`CANON.md`](CANON.md) or the H4-qualified compiler contracts.

## Platform relationship

UMG is larger than the compiler:

```text
Authoring / Applications
        ↓
UMG Platform / Runtime
        ↓
compiler-vNext
        ↓
RuntimeSpec + Trace
        ↓
execution hosts / capabilities
        ↓
RuntimeEvents / Viewer / persistence
```

- compiler-vNext = semantic resolution authority
- Platform Runtime = runtime orchestration, state, policy, capabilities, persistence
- MCP / REST / SDK / CLI = access and integration surfaces
- Studio / Website = authoring, inspection, and visualization
- Hermes / OpenClaw / Codex / models = host and integration layers

## Status

UMG remains under active development. Current compiler-vNext v0.1 semantics are frozen at H4 while the surrounding Platform, integrations, libraries, Studio, documentation, and experimental research continue to evolve.
