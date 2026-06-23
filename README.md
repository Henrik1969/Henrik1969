# Hi, I'm Henrik

I build small tools, language experiments, and Linux/C++ utilities because I enjoy understanding how things work from the inside.

My main interests are:

- C and C++
- Linux tooling
- SQL / data layers
- command-line utilities
- programming language design and implementation
- compiler/toolchain experiments

Table of contents

- [Flowcore](#flowcore)
  - [flowmini v22 — Unit Kinds (latest)](#flowmini-v22---unit-kinds-latest)
  - [flowmini v21 — Structural Bridge](#flowmini-v21---structural-bridge)
  - [flowmini v20 — Bool / predicate result](#flowmini-v20---bool--predicate-result)
  - [flowmini v19 — Comments](#flowmini-v19---comments)
  - [flowmini v16 — ABI pointer contracts](#flowmini-v16---abi-pointer-contracts)
  - [flowmini v15 — ABI bindings (proof-of-concept)](#flowmini-v15---abi-bindings-proof-of-concept)
  - [flowmini v13 — Imports / reusable libraries](#flowmini-v13---imports--reusable-libraries)
  - [flowmini v12 — `fn` value-bound ports](#flowmini-v12---fn-value-bound-ports)
  - [flowmini v10 — compound expressions](#flowmini-v10---compound-expressions)
  - [flowmini v9 — break / continue](#flowmini-v9---break--continue)
  - [flowmini v8 — list indexing frontend](#flowmini-v8---list-indexing-frontend)
  - [flowmini v7 — primitive if/else frontend](#flowmini-v7---primitive-ifelse-frontend)
  - [flowmini v6 — scopes / structured blocks](#flowmini-v6---scopes--structured-blocks)
  - [flowmini v5 — sweet `.flow` frontend](#flowmini-v5---sweet-flow-frontend)
  - [flowmini v4 — indexed memory / lists](#flowmini-v4---indexed-memory--lists)
  - [flowmini v3 — primitive core + derived atoms](#flowmini-v3---primitive-core--derived-atoms)
  - [flowmini v2 — generalized primitive graph model](#flowmini-v2---generalized-primitive-graph-model)
  - [flowmini v1 — minimal policy-envelope experiment](#flowmini-v1---minimal-policy-envelope-experiment)
  - [Structural subprojects](#structural-subprojects)
- [Other public repositories](#other-public-repositories)
- [Older / inactive repositories](#older--inactive-repositories)
- [Contact](#contact)

## Flowcore

- [**Flowcore / flowmini**](https://github.com/Henrik1969/Flowcore) — experimental graph/contract/flow-oriented programming language. The current prototype is Flowmini.

Status: Unstable / experimental (latest stage: flowmini v22). Earlier stages and structural subprojects are provided for reference and development history and are linked below. Subprojects (TokenTree, SymbolTable, etc.) are experimental but self-contained and are preconditions for future refactors — they can be reused in other projects.

### flowmini stages

- [flowmini v22 — Unit Kinds (latest)](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v22_unit_kinds/README.md) — first hard source-role boundary (program vs unit), categorized examples layout, and a test-oriented example runner. Status: Unstable / experimental (latest).

- [flowmini v21 — Structural Bridge](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v21_structural_bridge/README.md) — consolidates structural subprojects (TokenTree, SymbolTable) and exposes inspection/dump modes; builds the seam for the frontend refactor. Status: Reference / development history.

- [flowmini v20 — Bool / predicate result](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v20_bool/README.md) — introduces Bool as a real value type (true/false), comparisons produce Bool, and Bool can be used in variables, prints, and function signatures. Status: Reference / development history.

- [flowmini v19 — Comments](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v19_comments/README.md) — adds `//` and nested `/* ... */` block comments and related parser/lowerer handling. Status: Reference / development history.

- [flowmini v16 — ABI pointer contracts](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v16_abi_pointer_contracts/README.md) — formalizes pointer-shaped ABI values as sealed contracts within an `abi` block; pointer manipulation remains restricted to ABI boundaries. Status: Reference / development history.

- [flowmini v15 — ABI bindings (proof-of-concept)](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v15_abi_bindings/README.md) — narrow ABI bridge to shared libraries (dlopen/dlsym) to treat external symbols as node-like callable contracts. Status: Reference / development history.

- [flowmini v13 — Imports / reusable libraries](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v13_imports/README.md) — adds `import "file.flow"` so reusable function libraries and std files can be placed outside the main file; import rules and negative tests included. Status: Reference / development history.

- [flowmini v12 — `fn` value-bound ports](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v12_fn_value_ports/README.md) — function declarations modeled as reusable node templates with value-bound argument/return ports; non-recursive calls, inlining/instantiation lowering. Status: Reference / development history.

- [flowmini v10 — compound expressions](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v10_compound_expressions/README.md) — adds compound value expressions while preserving a separate predicate/control layer and demonstrates lowering to explicit primitive graph IR. Status: Reference / development history.

- [flowmini v9 — break / continue](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v9_break_continue/README.md) — primitive loop control (`break`, `continue`) with lowering semantics and smoke/diagnostic tests. Status: Reference / development history.

- [flowmini v8 — list indexing frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v8_list_indexing/README.md) — structured list/indexing sugar (`arr[i]` reads/writes), `len` expressions, and start-record producers for pure examples. Status: Reference / development history.

- [flowmini v7 — primitive if/else frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v7_if_else/README.md) — adds `if { } else { }` structured control and branch semantics; lowers to explicit graph join nodes. Status: Reference / development history.

- [flowmini v6 — scopes / structured blocks](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v6_scopes/README.md) — adds `main { ... }`, lexical scopes, initialized declarations, and basic expressions; enforces declaration/assignment/shadowing rules. Status: Reference / development history.

- [flowmini v5 — sweet `.flow` frontend](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v5_frontend/README.md) — human-facing sugar that lowers into explicit `.flowir`, compact atom declarations, wire chains, and emit lowered IR mode. Status: Reference / development history.

- [flowmini v4 — indexed memory / lists](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v4_lists/README.md) — adds addressable indexed memory primitives (list.get/set/length) to support algorithms like sorting. Status: Reference / development history.

- [flowmini v3 — primitive core + derived atoms](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v3_layers/README.md) — separates need-to-have primitives from nice-to-have derived atoms and demonstrates lowering of derived atoms to primitives. Status: Reference / development history.

- [flowmini v2 — generalized primitive graph model](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v2_general/README.md) — moves toward a generalized primitive model with Record payloads and primitive atom composition. Status: Reference / development history.

- [flowmini v1 — minimal policy-envelope experiment](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v1_pattern_introduction/README.md) — the minimal experiment proving the Flow Policy Envelope Pattern: tiny lexer/parser -> graph -> runtime traversal. Status: Reference / development history.

### Structural subprojects

- [TokenTree](https://github.com/Henrik1969/Flowcore/blob/main/subprojects/TokenTree/) — lossless token/group tree structural library used during the frontend refactor. Experimental but self-contained; reusable.
- [SymbolTable](https://github.com/Henrik1969/Flowcore/blob/main/subprojects/SymbolTable/) — policy-free symbol/fact/scope storage used for inspection and semantic layers. Experimental but self-contained; reusable.

Examples and running notes

- Build Flowcore/Flowmini:

```bash
cmake -S . -B build
cmake --build build -j20
```

- Run examples with flowmini (flowmini currently reads input only via stdin, except for flags):

```bash
echo 5 | ./build/flowmini examples/countdown_structured.flow
# or
echo 0 | ./build/flowmini examples/bubblesort_compound.flow
```

Use the example files linked from each stage README. The general invocation pattern is to pipe example input into flowmini via stdin.

## Other public repositories

- [ckb-next](https://github.com/Henrik1969/ckb-next) — RGB Driver for Linux (fork)
- [ggerganov_llama.cpp](https://github.com/Henrik1969/ggerganov_llama.cpp) — fork of ggerganov's llama.cpp
- [json](https://github.com/Henrik1969/json) — JSON for Modern C++ (fork)

## Older / inactive repositories

- **AppEssentials** — earlier utility experiments, mostly superseded now.
- **EnvVar** — environment-variable utility work; not fully updated at the moment.

I am a hobbyist developer. I build because I find it interesting, because it teaches me things, and because I can.

## Contact

Email: henriksorensen1969@gmail.com

Please include `githubbuddy` in the subject line so I can sort it properly.
