# Safety & Symbolic Execution

One of ZZ's most distinctive features is its approach to safety: **all safety checks are performed at compile time using formal verification**, with zero runtime overhead.

## How It Works

ZZ converts your code into **SSA (Static Single Assignment) form** and executes it symbolically inside an **SMT (Satisfiability Modulo Theories) solver** — either Z3 or Yices.

The solver checks whether any execution path could lead to undefined behavior according to the C standard. If it can, the compiler rejects the code with an error.

Because all checks happen at compile time:
- No runtime bounds checks are emitted
- No runtime null checks are emitted
- The generated C is lean and fast

## What Is Checked

ZZ verifies:

- **Array bounds** — array accesses must be proven in-bounds
- **Pointer validity** — pointer dereferences must be proven safe
- **Integer overflow** — arithmetic must be proven not to overflow (when relevant)
- **Preconditions** — function `@requires` annotations
- **Postconditions** — function `@ensures` annotations
- **Invariants** — loop and data structure invariants

## Raw Pointers Are Fine

ZZ allows raw unchecked pointers — just like C. The difference is that ZZ requires you to have **mathematical proof** that your pointer usage is defined behavior.

If the solver cannot prove safety, the compiler errors:

