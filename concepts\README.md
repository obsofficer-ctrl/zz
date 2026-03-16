# Core Concepts

This section explains the fundamental concepts of the ZZ language.

## Overview

ZZ is a C dialect with:

- **Go and Rust aesthetics** — clean syntax, explicit ownership hints
- **Plain C semantics** — raw pointers, manual memory management, no hidden costs
- **Formal verification** — all safety checks happen at compile time via SMT solving

ZZ does not have:
- A garbage collector
- Stack unwinding / exceptions
- Coroutines
- Hidden allocations

Everything ZZ does compiles to readable, standard C.

## Topics

- [Safety & Symbolic Execution](safety.md)
- [Types & Memory](types-and-memory.md)
- [Functions](functions.md)
- [Structs](structs.md)
- [Modules](modules.md)
- [Visibility](visibility.md)
