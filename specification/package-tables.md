---
title: Package tables
parent: Specification
---

**Package tables** are the primary way of setting up packages with unicornpkg. They are a Lua table or a function that returns a Lua table.

The only required fields are `name` and `pkgType`, but more are recommended if you want your package to be useful.

## Fields
### `unicornSpec`

This specifies the version of the package table. This should always be set to `v1.0.0`.

### `name`

This should be the same as the filename without the `.lua` extension.

### `pkgType`

Specifies the package type; see [Package providers](./package-providers/index.md) for more information.

The string is formatted based on the domain of the provider; for example, GitHub's provider is `com.github`, and Bitbucket's provider is `org.bitbucket`.

### `instdat`

A table that contains information specific to the `pkgType`. See individual [package providers](./package-providers/index.md) for more information.

### `rel`

A table that contains information relating to other packages.

#### `rel.depends`

An ordered table that lists required packages.
