---
title: How to install a raw package
parent: How-tos
nav_order: 3
---

This guide will cover installing a package without using a remote.

This guide assumes you have a working install of libunicorn and unicorntool.

1. Download your package. Use a tool like `wget` to download the package table.
2. Install your package with `unicorntool install full/path/to/package.lua`. This is the main command to install a package.
3. Play with your package. The package most likely got installed to `/lib` or `/bin`; check one of those directories and play around with it!
4. Remove your package with `unicorntool uninstall package-name`. The package name is in the source package. If it's an application, there is a good chance it's name is the name of the package.
