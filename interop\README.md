# Interoperability

One of ZZ's core design goals is seamless interoperability with C. ZZ compiles to plain C, so integration with existing C codebases is straightforward.

## Topics

- [Using C Libraries](using-c-libraries.md)
- [Exporting to C](exporting-to-c.md)

## Key Points

- ZZ emits standard ANSI C with no special runtime requirements
- Generated headers follow C conventions and can be included in any C project
- ZZ functions marked `export` are accessible from C without any glue code
- C functions and headers can be used from ZZ with `using`
- No ABI mismatch — ZZ uses the plain C calling convention
