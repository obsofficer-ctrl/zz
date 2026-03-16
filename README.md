# ZetZ (ZZ) Language Documentation

Welcome to the ZetZ (ZZ) language documentation. ZZ is a systems programming language targeting bare metal MCUs, embedded Linux, WASM, and other environments where C is the de facto standard.

## What is ZZ?

ZZ is a safe systems programming language that compiles to plain C. It provides:

- **Formal verification** via symbolic execution at compile time (no runtime overhead)
- **Plain C ABI** — just include the header in any C project
- **Stack-based memory** — no heap allocation required
- **Namespace management** — automatic header generation and declaration ordering
- **Interoperability** — works with any C compiler, including vendor-specific toolchains

## Who is ZZ for?

ZZ is designed for developers who:

- Work on systems without dynamic memory
- Need to produce C-compatible libraries
- Want safety guarantees without runtime cost
- Target embedded systems, MCUs, WASM, or bare-metal environments

## Documentation Overview

- [Prerequisites](getting-started/prerequisites.md)
- [Installation & Setup](getting-started/installation.md)
- [Hello World](getting-started/hello-world.md)
- [Project Structure](getting-started/project-structure.md)
- [Building & Running](getting-started/building.md)
- [Core Concepts](concepts/README.md)
  - [Safety & Symbolic Execution](concepts/safety.md)
  - [Types & Memory](concepts/types-and-memory.md)
  - [Functions](concepts/functions.md)
  - [Structs](concepts/structs.md)
  - [Modules](concepts/modules.md)
  - [Visibility](concepts/visibility.md)
- [Dependencies](dependencies/README.md)
  - [zz.toml](dependencies/zz-toml.md)
  - [User Space Repositories](dependencies/user-space-repositories.md)
- [Interoperability](interop/README.md)
  - [Using C Libraries](interop/using-c-libraries.md)
  - [Exporting to C](interop/exporting-to-c.md)
- [Formal Verification](verification/README.md)
  - [Z3 & Yices](verification/z3-yices.md)
  - [Assertions & Invariants](verification/assertions.md)
- [Standard Library](stdlib/README.md)
- [Examples](examples/README.md)

## Community

- [Discord](https://discord.gg/EsMxjWtcf5)
- [GitHub](https://github.com/zetzit/zz)

## Editor Support

- **Emacs**: [zetz-mode](https://github.com/damon-kwok/zetz-mode)
- **Vim**: [zz.vim](https://github.com/zetzit/vim)
