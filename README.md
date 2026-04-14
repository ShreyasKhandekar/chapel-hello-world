# 'Hello, world!' in Chapel

[Chapel](https://github.com/chapel-lang/chapel/) is a programming language for productive parallel computing. This repository is a simple starting point for Chapel in GitHub Codespaces, with runnable examples in [examples/](examples).

> ⚠️ **Warning:** Codespaces runs in a virtualized environment with shared hardware and a modest core count. Performance and available parallelism in Codespaces are not representative of what you should expect on a native Chapel installation.

## Compile And Run In The Terminal

Compile and run the main hello-world program:

```bash
chpl hello.chpl
./hello
```

Compile and run one of the included examples:

```bash
chpl examples/hello3-datapar.chpl
./hello3-datapar
```

## Simulated Distributed (Multi-Locale) Runs

The Codespace defaults to single-locale mode (`CHPL_COMM=none`).

To simulate multi-locale execution, compile with `CHPL_COMM=gasnet`:

```bash
CHPL_COMM=gasnet chpl examples/hello4-datapar-dist.chpl
./hello4-datapar-dist -nl 2
```

Or export once per shell and compile as usual:

```bash
export CHPL_COMM=gasnet
chpl examples/hello4-datapar-dist.chpl
./hello4-datapar-dist -nl 2
```

## Learn More And Try More Programs

You can copy in additional examples from Chapel Primers or Chapel tutorial/example programs to explore more language features.

- [Learning Chapel](https://chapel-lang.org/learning.html)
- [Chapel Primers](https://chapel-lang.org/docs/primers/)
- [Chapel tutorial examples](https://github.com/chapel-lang/chapel/tree/main/test/exercises/Oct2023tutorial)
- [Multilocale Chapel Execution](https://chapel-lang.org/docs/usingchapel/multilocale.html)
- [Download Chapel](https://chapel-lang.org/download.html)
