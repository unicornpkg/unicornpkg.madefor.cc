---
title: Package providers
parent: Specification
has_children: true
---

**Package providers** are the workhorse of unicornpkg; they allow you to use various online services to install packages.

The built-in package providers are [`com.pastebin`](./com.pastebin.md), [`dev.devbin`](./dev.devbin.md), [`com.github`](./com.github.md), [`com.github.gist`](./com.github.gist.md), [`com.gitlab`](./com.gitlab.md), and [`org.bitbucket`](./org.bitbucket.md).

Custom package providers can be created by having a `.lua` file in the `/lib/unicorn/provider` directory. That Lua file should return a single function which takes one argument (a package table) and installs a package table upon being called, with no interactive prompting.
