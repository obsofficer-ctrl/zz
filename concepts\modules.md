# Modules

ZZ organizes code into modules. Each `.zz` file is a module.

## Automatic Module Discovery

All `.zz` files in your `src/` directory are automatically part of your project. ZZ discovers them without explicit registration.

## Module Names

A file's module name is derived from its filename and project name:

- Project `myproject`, file `src/utils.zz` → module `myproject::utils`
- Project `myproject`, file `src/main.zz` → module `myproject` (root)

## Using Items from Other Modules

Use the `using` keyword to bring items into scope:

