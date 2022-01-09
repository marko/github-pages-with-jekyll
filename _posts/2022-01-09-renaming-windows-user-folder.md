---
title: "Renaming Windows user folder"
date: 2022-01-09
---

A few years ago I switched from a local Windows account to signing in with my Microsoft account. 
The user folder name (`C:\Users\<name>`) has remained unchanged since then.
Today I finally decided to change it. Here's how:


1. Logged in on a different admin account
2. Found the SID for my primary account with `wmic useraccount get name,SID`
3. Used regedit to change the `ProfileImagePath` to my new username at `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList\<SID>`
4. Renamed the user profile folder

This was probably stupid. At least two programs broke (OneDrive and VSCode). Reinstalled them instead of troubleshooting. 
