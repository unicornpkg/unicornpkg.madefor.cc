---
title: Package tables
---

**Package tables** are the primary way of setting up packages with unicornpkg. They are a Lua table or a function that returns a Lua table.

The only required fields are `name` and `pkgType`, but more are recommended if you want your package to be useful.

## Fields
### `name`

This should be the same as the filename without the `.lua` extension.

### `pkgType`

Specifies the package type; see [Package providers](./Package providers) for more information.

The string is formatted based on the domain of the provider; for example, GitHub's provider is `com.github`, and Bitbucket's provider is `org.bitbucket`.

### `instdat`

A table that contains information specific to the `pkgType`. See individual [package providers](./Package providers/index.md) for more information.
