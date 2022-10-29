---
title: Package remotes
---

**Package remotes** are a feature in unicornpkg that allow you to download package tables semi-automatically.

## Specification
### Remote

The remote is a simple HTTP server. It's usually a GitHub repository, but other hosts should work fine.

Each package should be a file on the package remote ending in `.lua`.

The remote should contain a file called "unicorn.txt" that contains the name of all packages present on that remote, **without the `.lua` suffix**.

### Retrieval on the client

The client will have a folder called `/etc/unicorn/remotes/` that will contain one serialised file per remote. Each serialised file should contain a `url` keyword specifiying the full HTTP path to the remote, as well as a `packages` table that contains known packages from that remote.

`unicorn.remote.update()` should parse each file in `/etc/unicorn/remotes` and update the `packages` table.

`unicorn.remote.get()` should parse each file in `/etc/unicorn/remotes/` and download the requested file to `/tmp/unicorn/{package_name}.lua`, and then `unicorn.install()` should install said file.
