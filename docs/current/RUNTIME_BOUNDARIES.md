# Runtime and Authority Boundaries

UMG separates authored semantics, compiler resolution, runtime orchestration, execution, and observability.

## Authority chain

```text
Authored Sleeve + explicit Selection
        ↓
compiler-vNext
        ↓
RuntimeSpec + Trace + diagnostics
        ↓
Platform Runtime / host execution
        ↓
RuntimeEvents / results / persisted state
```

## Important distinctions

### Compiler Trace vs RuntimeEvents

- Trace explains compiler resolution and derivation.
- RuntimeEvents record execution-time behavior.
- RuntimeEvents must not be treated as a rewrite of compiler semantics.

### RuntimeSpec vs execution

RuntimeSpec is an executor-facing specification. It does not itself execute a model or tool.

### Evidence vs authority

Retrieved evidence, RAG passages, ToolResults, and external data are input/evidence. They do not become Directive, Instruction, Philosophy, Governance, or tool permission merely by being retrieved.

### Platform state vs authored Sleeve

Runtime state may change during a session. It does not silently mutate the authored Sleeve.

### Persona/runtime adaptation vs compiler lanes

Persona, Mutable Persona state, DSG, Use/Aim/Need, and other runtime/controller research may exist above or beside the compiler contract. They are not automatically compiler-vNext MOLT lanes or v0.1 Sleeve fields.

## Consumer responsibilities

- Platform Runtime owns sessions, runtime state, Needs, execution orchestration, policy, and persistence.
- MCP / REST / SDK / CLI expose services and projections.
- Studio / Website author, inspect, and visualize.
- Hermes / OpenClaw / Codex / models act as host or integration layers.
- compiler-vNext remains semantic resolution authority for current v0.1 compilation.

