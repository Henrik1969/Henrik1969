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
  - [flowmini v12 — fn value-bound ports](#flowmini-v12---fn-value-bound-ports)
  - [flowmini v10 — compound expressions](#flowmini-v10---compound-expressions)
- [Other public repositories](#other-public-repositories)
- [Older / inactive repositories](#older--inactive-repositories)
- [Contact](#contact)

## Flowcore

- [**Flowcore / flowmini**](https://github.com/Henrik1969/Flowcore) — experimental graph/contract/flow-oriented programming language (unstable, experimental). The current prototype is Flowmini.

  Status: Unstable / experimental (latest stage: flowmini). Earlier stages are kept for reference and development history and are linked below.

  Staged READMEs:

  - [flowmini v12 — fn value-bound ports](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v12_fn_value_ports/README.md) — introduces a first function layer (value-bound argument/return ports), non-recursive calls, and an explicit lowering model for functions. Status: Unstable / experimental.
  - [flowmini v10 — compound expressions](https://github.com/Henrik1969/Flowcore/blob/main/Flowmini/flowmini_v10_compound_expressions/README.md) — adds compound value expressions while preserving a separate predicate/control layer and demonstrates lowering to an explicit primitive graph IR. Status: Reference / development history.

  Examples and running notes

  - Build:

    ```bash
    cmake -S . -B build
    cmake --build build -j20
    ```

  - Run examples with flowmini (flowmini currently accepts input only via stdin, except for flags):

    ```bash
    echo 5 | ./build/flowmini examples/compound_expression_demo.flow
    # or
    echo 0 | ./build/flowmini examples/bubblesort_compound.flow
    ```

    Use the example files linked from each stage README. The above shows the general invocation pattern: provide input on stdin (for example numeric input) and flowmini reads it from stdin.

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
