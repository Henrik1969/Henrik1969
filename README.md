# Hi, I'm Henrik

I'm a hobbyist developer who builds small libraries, language experiments, and Linux/systems-level utilities. I work mainly in C and C++, focusing on understanding how things work from the inside — especially around configuration, tooling, data layers, contracts, and runtime behavior.

## What I build

- **C and C++** libraries and tools (modern standards, systems-level)
- **Linux tooling** and command-line utilities
- **Configuration and environment management** systems
- **SQL / data layers** and structured storage
- **Language design and compiler experiments**
- **Systems modeling** through contracts, policies, and explicit boundaries
- **Reusable library bricks** for parsing, symbols, AST work, and capability-style design

## Current projects

### ConfigResolve

A C++20 configuration resolution engine for layered sources, validation, provenance tracking, governed runtime stores, scoped subsystem views, runtime mutation, diagnostics, and stable C ABI bindings.

- [ConfigResolve repository](https://github.com/Henrik1969/ConfigResolve)

### Flowcore

An experimental language/system-architecture project centered on explicit contracts, source structure, ASTs, graph-shaped execution, policy envelopes, lowering layers, and systems modeling.

Current active line:

```text
Flowmini v0.24 explicit AST
```

- [Flowcore repository, active branch](https://github.com/Henrik1969/Flowcore/tree/v24-explicit-ast)
- [Flowcore development notes (below)](#flowcore-development)

### EnvVar

A C++ environment-variable utility and library experiment focused on structured access, snapshots, search, diffing, and shell ergonomics — all while preserving normal Unix environment semantics.

- [EnvVar repository](https://github.com/Henrik1969/EnvVar)

### SymbolTable

A C++20 policy-free symbol table library designed for language and compiler experiments, separating storage and semantics concerns.

- [SymbolTable repository](https://github.com/Henrik1969/Flowcore/tree/v24-explicit-ast/subprojects/SymbolTable)

### ArgsLib / AstLib

Small, focused C++ library bricks for argument parsing and AST / data-structure work. Designed to be composable and reusable across projects.

### Other public repositories

- [ckb-next](https://github.com/Henrik1969/ckb-next) — RGB Driver for Linux (fork)
- [ggerganov_llama.cpp](https://github.com/Henrik1969/ggerganov_llama.cpp) — fork of ggerganov's llama.cpp
- [json](https://github.com/Henrik1969/json) — JSON for Modern C++ (fork)

## Flowcore development

## Flowcore development

Flowcore is my experimental language/system-architecture project.

The current active line is:

```text
Flowmini v0.24 explicit AST
branch: v24-explicit-ast
```

At the surface, early Flowmini examples may look like a small conventional programming language. That is intentional. The current work is not novelty syntax first; it is the layered model underneath:

```text
source text
    -> tokens
    -> source structure
    -> explicit AST
    -> semantic facts
    -> contracts/scopes
    -> graph-shaped IR
    -> executable system projection
```

Current v0.24 status:

```text
AST golden tests: PASS (8)
Flowmini suite:   PASS (76/76)

status: experimental
production-ready: no
```

Start here:

- [Flowcore repository, active branch](https://github.com/Henrik1969/Flowcore/tree/v24-explicit-ast)
- [Flowmini README](https://github.com/Henrik1969/Flowcore/blob/v24-explicit-ast/Flowmini/README.md)
- [Current Flowmini status](https://github.com/Henrik1969/Flowcore/blob/v24-explicit-ast/Flowmini/CURRENT.md)
- [Flowmini v0.24 explicit AST status](https://github.com/Henrik1969/Flowcore/blob/v24-explicit-ast/Flowmini/flowmini_v24_explicit_ast/docs/v0.24-explicit-ast-status.md)
- [Flowmini v0.24 shallow expression AST SITREP](https://github.com/Henrik1969/Flowcore/blob/v24-explicit-ast/Flowmini/flowmini_v24_explicit_ast/docs/v0.24-shallow-expression-ast-sitrep.md)
- [Flowmini version index](https://github.com/Henrik1969/Flowcore/blob/v24-explicit-ast/Flowmini/VERSION_INDEX.md)

Older Flowmini stages are preserved as historical development material, but they are no longer the active public entry point.

## Contact

Email: henriksorensen1969@gmail.com

Please include `githubbuddy` in the subject line so I can sort it properly.

---

I build because I find it interesting, because it teaches me things, and because I can.
