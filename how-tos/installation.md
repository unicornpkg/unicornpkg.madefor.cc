---
title: How to install unicornpkg
parent: How-tos
---

In this how-to guide, we will install libunicornpkg and unicorntool onto a computer.

This guide requires access to the HTTP API.

1. Execute `wget run https://raw.githubusercontent.com/unicornpkg/wing/main/install.lua`. This script bootstraps Wing onto your system. Wing is the official distribution of unicornpkg.
2. Add `/bin` to your `shell.path`. There is a script to bootstrap this, available by executing `wget https://raw.githubusercontent.com/unicornpkg/unicornpkg-main/main/unix-path-bootstrap.lua`, `/bin/unicorntool install unix-path-boostrap.lua`, and then restart your system.
3. You're done! Check out other how-tos.
