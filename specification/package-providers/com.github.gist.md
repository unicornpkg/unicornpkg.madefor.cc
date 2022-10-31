---
title: com.github.gist
parent: Package providers
grand_parent: Specification
---

`com.github.gist` is the identifier for the package provider of [GitHub Gists](https://gists.github.com).

This provider enables sourcing the contents of a single-file GitHub Gist (ergo, a Gist with only one file).

### `instdat.repo_owner`

The owner of the target Gist.

### `instdat.repo_name`

The identifier of the target Gist. (This is named this way for consistency with [com.github](./com.github.md) and because Gists are technically repositories.)

### `instdat.repo_ref`

A valid commit inside of the target Gist.

