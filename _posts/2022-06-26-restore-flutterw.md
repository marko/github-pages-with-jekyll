---
title: "Restore flutterw"
date: 2022-06-26
---

`flutterw` uses a git submodule to sync the Flutter version. I ran an upgrade prematurely, that I had to restore. `git restore` doesn't handle submodules, but [this script](https://stackoverflow.com/a/27415757/4600706) worked:
```sh
git submodule deinit -f .
git submodule update --init
```
