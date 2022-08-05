---
layout: post
title:  "Powershell Cheatsheet"
date:   2022-08-05 11:45:00 +0100
categories: Programming
tags: powershell, cheatsheet, windows
---
# Overview
A handy compilation of basic powershell stuff that I always forget!

## Display an Environment Variable
```powershell
$env:<env variable>
```
### Display Path
```powershell
$env:Path              # Display path
$env:Path.split(";")   # Display separated path
```
