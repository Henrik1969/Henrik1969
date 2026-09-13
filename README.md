# Hi, I'm Henrik

I'm a hobbyist developer who builds small libraries, language experiments, and Linux/systems-level utilities. I work mainly in C and C++, focusing on understanding how things work from the inside.

## What I build

- **C and C++** libraries and tools (modern standards, systems-level)
- **Linux tooling** and command-line utilities
- **Configuration and environment management** systems
- **Text data structures** for mutation, history, and transactions
- **Language design and compiler experiments**
- **Systems modeling** through contracts, policies, and explicit boundaries
- **Reusable library bricks** for parsing, symbols, AST work, and capability-style design

## Current projects

### ConfigResolve

A C++20 configuration resolution engine for layered sources, validation, provenance tracking, governed runtime stores, scoped subsystem views, runtime mutation, diagnostics, and stable C ABI bindings.

**Status**: Stable. v1.1.0 released under the ConfigResolve name (renamed from earlier `configlib`). Full CMake/pkg-config integration, Debian packaging, and comprehensive documentation.

- [ConfigResolve repository](https://github.com/Henrik1969/ConfigResolve)

### Flowcore

An experimental graph/contract/flow-oriented programming language project centered on explicit contracts, source structure, ASTs, graph-shaped execution, policy envelopes, lowering layers, and systems modeling.

**Status**: Experimental, unstable, not production-ready. Currently contains flowmini prototype versions and syntax experiments. Repository is a raw design/implementation workspace.

Current active version:
```text
Flowmini/flowmini_v29_reusable_native_chain
```

- [Flowcore repository](https://github.com/Henrik1969/Flowcore)
- [Flowmini README](https://github.com/Henrik1969/Flowcore/blob/master/Flowmini/README.md)

### TextLib

A C++20, representation-independent text abstract data type for editors, viewers, parsers, command-line tools, collaboration systems, and other software needing dependable structural text mutation.

**Status**: Active development. Provides adaptive storage, full mutation API, replayable changes, undo/redo through transactions, and extensive test coverage (GCC, Clang, ASan, UBSan, field tests, allocation-failure tests).

- [TextLib repository](https://github.com/Henrik1969/TextLib)

### FrankenCore

A constitutional umbrella and governance layer for a family of independently owned projects. Owns shared architectural policies, cross-project contracts, and shared tooling rather than private implementations.

**Status**: Early-stage constitutional organization. Establishes canonical architectural laws and cross-project conformance rules. Current children include Flowcore and FrankenPOP (independent repositories).

- [FrankenCore repository](https://github.com/Henrik1969/FrankenCore)

### SymbolTable

A C++20 policy-free symbol table library designed for language and compiler experiments, separating storage and semantics concerns.

**Status**: Experimental. Developed within Flowcore as a reusable library brick. Located in Flowcore's subprojects directory.

- [SymbolTable in Flowcore](https://github.com/Henrik1969/Flowcore/tree/master/subprojects/SymbolTable)

### Other public repositories

- [ckb-next](https://github.com/Henrik1969/ckb-next) — RGB Driver for Linux (fork)
- [ggerganov_llama.cpp](https://github.com/Henrik1969/ggerganov_llama.cpp) — fork of ggerganov's llama.cpp
- [json](https://github.com/Henrik1969/json) — JSON for Modern C++ (fork)

## Notes on project maturity

- **Stable**: ConfigResolve
- **Active development**: TextLib
- **Experimental**: Flowcore (language design workspace), FrankenCore (constitutional umbrella)
- **Archive/Reference**: Forks and historical repositories

## Contact

Email: henriksorensen1969@gmail.com

Please include `githubbuddy` in the subject line so I can sort it properly.

---

I build because I find it interesting, because it teaches me things, and because I can.
