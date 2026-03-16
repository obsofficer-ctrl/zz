# Visibility

ZZ has three visibility levels that control where a symbol can be used.

## `export`

`export` makes a symbol part of the public API. It is visible to:
- Other ZZ modules
- External C code (included in generated headers)
- The linker

