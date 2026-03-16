# User Space Repositories

ZZ supports fetching dependencies from any Git repository. You are not limited to an official package registry — any accessible Git URL works.

## How It Works

When you declare a dependency in `zz.toml`, ZZ:

1. Clones the Git repository (or updates it if already cached)
2. Looks for the module in the repository's `src/` directory
3. Makes it available under the declared name

## Declaring a Dependency

