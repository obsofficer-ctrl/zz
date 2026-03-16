# Types & Memory

ZZ uses C's type system as a foundation, adding a few conveniences and safety abstractions.

## Primitive Types

ZZ uses explicit-width integer types (similar to Rust):

| ZZ Type | C Equivalent | Description |
|---------|-------------|-------------|
| `u8`    | `uint8_t`   | Unsigned 8-bit integer |
| `u16`   | `uint16_t`  | Unsigned 16-bit integer |
| `u32`   | `uint32_t`  | Unsigned 32-bit integer |
| `u64`   | `uint64_t`  | Unsigned 64-bit integer |
| `i8`    | `int8_t`    | Signed 8-bit integer |
| `i16`   | `int16_t`   | Signed 16-bit integer |
| `i32`   | `int32_t`   | Signed 32-bit integer |
| `i64`   | `int64_t`   | Signed 64-bit integer |
| `int`   | `int`       | Platform int |
| `uint`  | `unsigned int` | Platform unsigned int |
| `usize` | `size_t`    | Platform pointer-sized unsigned integer |
| `bool`  | `bool`      | Boolean |
| `char`  | `char`      | Character |
| `void`  | `void`      | No value |

## Pointers

Pointers in ZZ work exactly like C:

