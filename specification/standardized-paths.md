---
title: Standardized paths
parent: Specification
---

unicornpkg recommends the following paths for package contents:

- `/bin` for executable Lua files. This path should be on `shell.path`.
- `/lib` for modules, APIs, and libraries. This path should be on `package.path` if you're writing complementary software.
- `/etc/help/` for help files. This path should be on `help.path`.
- `/home` for user data, or `home/{user}` if you are writing a multi-user system.

If your use-case is not specified here, follow the POSIX specification.
