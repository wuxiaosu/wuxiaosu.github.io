---
title: "Android 8.0 以上开启全局可调式"
date: 2022-04-12T17:21:00+08:00
draft: false
tags: ["android"]
---
# Android 8.0 以上开启全局可调式  

- 1.安装好 Magisk

- 2.终端执行

```bash
adb shell
```  

```bash
su
```  

```bash
magisk resetprop ro.debuggable 1
```  

- 3.重启 system server

```bash
stop;start
```  

- 4.重启手机会失效
