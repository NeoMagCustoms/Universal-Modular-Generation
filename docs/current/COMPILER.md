# UMG Compiler — Current Authority

## Current implementation

UMG's current compiler is **compiler-vNext v0.1.0-experimental**.

- Repository: `NeoMagnetar/umg-compiler-vnext`
- H4 commit: `c505f9a7f23010574733c8c03c4162af5317a5eb`
- H4 tag: `compiler-vnext-v0.1.0-experimental-h4-qualified`
- Qualification: C–H complete; H4 frozen

The historical `NeoMagCustoms/umg-compiler` compiler-v0 implementation is retired for new work.

## What the compiler owns

compiler-vNext owns:

- Sleeve validation
- Selection validation
- NeoStack topology validation
- NeoBlock/MOLT geometry validation
- deterministic resolution
- READY / ACTIVE / OFF / DISABLED final state
- Bundle handling
- supported Overlay handling
- Governance OFF
- Merge validation/provenance
- RuntimeSpec
- Trace
- diagnostics
- runtimeHash

## What the compiler does not own

compiler-vNext does not:

- interpret natural-language user intent
- call an LLM
- retrieve documents
- execute tools
- infer Trigger truth
- invent a Selection
- create application runtime sessions
- execute RuntimeSpec

Those responsibilities belong to caller/controller, Platform Runtime, adapters, and host systems.

## Current schemas

- Sleeve: `umg.compiler-vnext.sleeve.v0.1`
- Selection: `umg.compiler-vnext.selection.v0.1`
- RuntimeSpec: `umg.compiler-vnext.runtime.v0.1`
- Trace: `umg.compiler-vnext.trace.v0.1`
- CompileResult: `umg.compiler-vnext.compile-result.v0.1`

## Change policy

Do not change compiler-vNext v0.1 semantics to preserve a stale consumer. Fix or migrate the consumer instead.

A compiler semantic change requires either:

1. a proven defect repair within the frozen contract; or
2. an explicitly authorized future compiler version program.

