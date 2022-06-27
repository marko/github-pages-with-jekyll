---
title: "Restore flutterw"
date: 2022-06-26
---

`flutterw` uses a git submodule to sync the Flutter version. I ran an upgrade prematurely, that I had to restore. `git restore` doesn't handle submodules.
```sh
git submodule update 
```
