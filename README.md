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

An experimental programming language and runtime centered on explicit contracts, flows, graph structure, policy envelopes, lowering layers, and systems modeling. Currently prototyped as Flowmini with active development across multiple semantic stages.

- [Flowcore repository](https://github.com/Henrik1969/Flowcore)
- [Flowcore development notes (below)](#flowcore-development)

### EnvVar

A C++ environment-variable utility and library experiment focused on structured access, snapshots, search, diffing, and shell ergonomics — all while preserving normal Unix environment semantics.

- [EnvVar repository](https://github.com/Henrik1969/EnvVar)

### SymbolTable

A C++20 policy-free symbol table library designed for language and compiler experiments, separating storage and semantics concerns.

- [SymbolTable repository](https://github.com/Henrik1969/Flowcore/tree/main/subprojects/SymbolTable)

### ArgsLib / AstLib

Small, focused C++ library bricks for argument parsing and AST / data-structure work. Designed to be composable and reusable across projects.

### Other public repositories

- [ckb-next](https://github.com/Henrik1969/ckb-next) — RGB Driver for Linux (fork)
- [ggerganov_llama.cpp](https://github.com/Henrik1969/ggerganov_llama.cpp) — fork of ggerganov's llama.cpp
- [json](https://github.com/Henrik1969/json) — JSON for Modern C++ (fork)

## Flowcore development

Flowcore is in active but unstable experimental development. The prototype, Flowmini, progresses through versioned semantic stages, each introducing or refining language features.

### Latest stages

- [flowmini v22 — Unit Kinds](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v22_unit_kinds/README.md) — first hard source-role boundary (program vs unit), categorized unit declarations
- [flowmini v21 — Structural Bridge](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v21_structural_bridge/README.md) — consolidates structural subprojects (TokenTree, SymbolTable)
- [flowmini v20 — Bool / predicate result](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v20_bool/README.md) — Bool as a real value type, comparison predicates
- [flowmini v19 — Comments](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v19_comments/README.md) — line and nested block comments, parser/lowerer updates

### Earlier stages

- [flowmini v16 — ABI pointer contracts](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v16_abi_pointer_contracts/README.md) — sealed contracts for pointer-shaped ABI values
- [flowmini v15 — ABI bindings (proof-of-concept)](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v15_abi_bindings/README.md) — narrow ABI bridge to shared libraries (dlopen/dlsym)
- [flowmini v13 — Imports / reusable libraries](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v13_imports/README.md) — import statement for reusable function libraries
- [flowmini v12 — `fn` value-bound ports](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v12_fn_value_ports/README.md) — function declarations as reusable node templates
- [flowmini v10 — compound expressions](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v10_compound_expressions/README.md) — compound value expressions with graph structure preservation
- [flowmini v9 — break / continue](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v9_break_continue/README.md) — primitive loop control with lowering semantics
- [flowmini v8 — list indexing frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v8_list_indexing/README.md) — list/indexing sugar (arr[i]), length primitives
- [flowmini v7 — primitive if/else frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v7_if_else/README.md) — if/else structured control and branch semantics
- [flowmini v6 — scopes / structured blocks](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v6_scopes/README.md) — lexical scopes, initialized declarations, main blocks
- [flowmini v5 — sweet `.flow` frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v5_frontend/README.md) — human-friendly syntax lowering into explicit `.flowir`
- [flowmini v4 — indexed memory / lists](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v4_lists/README.md) — addressable indexed memory (list.get/set/length primitives)
- [flowmini v3 — primitive core + derived atoms](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v3_layers/README.md) — primitive vs derived atoms separation
- [flowmini v2 — generalized primitive graph model](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v2_general/README.md) — generalized primitives with Record types
- [flowmini v1 — minimal policy-envelope experiment](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v1_pattern_introduction/README.md) — proof-of-concept for Flow pattern

### Structural subprojects

- [TokenTree](https://github.com/Henrik1969/Flowcore/blob/main/subprojects/TokenTree/) — lossless token/group tree structural library for frontend refactoring
- [SymbolTable](https://github.com/Henrik1969/Flowcore/blob/main/subprojects/SymbolTable/) — policy-free symbol/fact/scope storage for inspection and semantic layers

### Building and running Flowcore

```bash
cmake -S . -B build
cmake --build build -j$(nproc)
```

Run examples (piping input via stdin):

```bash
echo 5 | ./build/flowmini examples/countdown_structured.flow
echo 0 | ./build/flowmini examples/bubblesort_compound.flow
```

See individual stage READMEs for example files and invocation patterns specific to each version.

## Contact

Email: henriksorensen1969@gmail.com

Please include `githubbuddy` in the subject line so I can sort it properly.

---

I build because I find it interesting, because it teaches me things, and because I can.
