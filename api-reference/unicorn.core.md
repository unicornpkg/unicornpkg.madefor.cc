---
title: unicorn.core
parent: API reference
---

Contains core logic for installing and uninstalling packages.

## install(package\_table)

Installs a raw package table.

### Example

Reads a package table from the disk and installs it.

**Insecure code warning: This will execute the file at `/tmp/example_package`.**

```lua
local unicorn = dofile("/lib/unicorn/init.lua")
local file_1 = fs.open("/tmp/example_package")
local contents = file_1.readAll()
unicorn.core.install(dofile(contents)) -- this is the insecure part. Don't do this if you don't trust the package!
```

## uninstall(package\_name)

Removes an installed package table from the system.

### Example

Removes an example package.

```lua
local unicorn = dofile("/lib/unicorn/init.lua")
unicorn.core.uninstall("example-package")
```

## See also

- [unicorn.core.provider](./unicorn.core.provider.md)

