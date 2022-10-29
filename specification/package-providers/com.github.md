---
title: com.github
parent: Package providers
grand_parent: Specification
---

`com.github` is the identifier for the package provider of [GitHub](https://github.com).

This provider enables sourcing individual files from a GitHub repository.

### `instdat.repo_owner`

The owner of the target repository.

### `instdat.repo_name`

The name of the target repository.

### `instdat.filemaps`

A table which contains mappings for files on GitHub and their local counterparts.

The key for each item in the table should correspond to the full path on the GitHub repository, and the value should be the local destination.

