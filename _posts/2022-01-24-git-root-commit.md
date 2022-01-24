---
title: Git root commit
date: 2022-01-25
---

Rebasing to change the first commit isn't possible. I now insert a null root commit. 
```git
git commit --allow-empty -m root
```

If you've already started adding real commits, move it with 
```git
git rebase -i --root
```
