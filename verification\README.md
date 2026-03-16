# Formal Verification

ZZ performs **formal verification at compile time** using SMT (Satisfiability Modulo Theories) solvers. This section explains how it works and how to use it effectively.

## Topics

- [Z3 & Yices](z3-yices.md)
- [Assertions & Invariants](assertions.md)

## What Is Formal Verification?

Formal verification means using mathematical proof to guarantee that your code is correct, rather than relying on testing alone.

ZZ uses **symbolic execution**: instead of running your code with specific inputs, it explores all possible inputs simultaneously and proves properties about the code's behavior.

## Key Insight

All verification happens at **compile time**. There is zero runtime overhead. The generated C contains no checks.

## What ZZ Verifies

- Array and buffer bounds
- Pointer safety
- User-defined preconditions (`@requires`)
- User-defined postconditions (`@ensures`)
- User-defined assertions (`@where`)
- Integer overflow (in certain contexts)
