---
title: unicorn.remote
parent: API reference
---

Documentation for using libunicornpkg's remote submodule.

## install(package\_name)
Installs a package from a remote.

This function traverses `/etc/unicorn/remotes` for all text files that contain URLs to a [package remote](../specification/package-remotes.md).

For each remote, it tries requesting the remote's URL plus the package's name. If it fails with a `Not Found` error, it moves on. If it gets a good response, then it installs the package.

### Example

```lua
local unicorn = dofile("/lib/unicorn/init.lua")\
unicorn.remote.install("aukit") -- installs MCJack123's AUKit, assuming the default remote is present
```
