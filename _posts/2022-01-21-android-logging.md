---
title: "logcat --pid"
date: 2022-01-21
---

A few days ago I had to capture live logs from an Android app I couldn't edit. There were no sensible tags to grep for. Luckily logcat supports filtering by process id!
```sh
adb logcat --pid=$(adb shell pidof -s app.bundle.id)
```
