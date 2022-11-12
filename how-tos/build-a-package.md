---
title: How to build a package
parent: How-tos
nav_order: 2
---

This how-to guide will cover how to create a custom package for unicornpkg.

This guide assumes you have a working executable file or a working library, along with a working install of libunicorn and unicorntool.

1. Create a file named `yourpackage.lua`. In most cases, name this the same name as your program.
2. Copy-and-paste the below boilerplate code into `yourpackage.lua`:

```lua
local package = {}
package.name = "yourpackage"
package.instdat = {}
package.instdat.filemaps = {}
package.instdat.filemaps["YOUR_PASTE_ID"] = "/bin/yourpackage.lua"
package.pkgType = "com.pastebin"
package.unicornSpec = "v1.0.0"

return package
```

If you need a custom folder (for a module, for example), add a `fs.makeDir` call before the `package` table is defined.
3. Test your package with `unicorntool`. See the [how-to guide for installing a raw package](./install-raw-package.md) to make sure your package works.
4. Share it! Open a PR on the main unicornpkg repository, or add it to a GitHub release with the `.unicornpkg.lua` extension.
