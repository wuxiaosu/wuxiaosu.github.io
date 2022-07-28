---
title: "使用MagiskHidePropsConf开启全局可调试"
date: 2022-01-129T17:00:34+08:00
draft: false
tags: ["MagiskHidePropsConf","android"]
---

## 1.安装好 Magisk  

此处略过

## 2.安装 MagiskHidePropsConf

+ 下载地址 <https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf/releases>
+ 安装完成后重启

## 3.按流程操作

+ 重启进入终端
+ 按流程一步一步操作就行了

```bash
adb shell
```

```bash
props
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 Select an option below.
=====================================

1 - Edit device fingerprint
2 - Force BASIC key attestation
3 - Device simulation (disabled)
4 - Edit MagiskHide props (active)
5 - Add/edit custom props
6 - Delete prop values
7 - Script settings
8 - Collect logs
u - Perform module update check
r - Reset all options/settings
b - Reboot device
e - Exit

See the module readme or the
support thread @ XDA for details.

Enter your desired option: 5
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 Custom props
 Select an option below:
=====================================

Set or edit custom prop values for your device.

Currently no custom props set.
Please add one by selecting
"New custom prop" below.

n - New custom prop
b - Go back to main menu
e - Exit

See the module readme or the
support thread @ XDA for details.

Enter your desired option: n
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 New custom prop
=====================================

Enter the prop to set. Example:
ro.sf.lcd_density

b - Go back
e - Exit

Enter your desired option: ro.debuggable
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 ro.debuggable
=====================================

ro.debuggable is
one of the sensitive props that can be
set by the MagiskHide props option.

Are you sure you want to proceed?

y - Yes
n - No
e - Exit

Enter your desired option: y
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 ro.debuggable
=====================================

Enter the value you want to set
ro.debuggable to,
or select from the options below.

The currently set value is:
0
Please enter the new value.

b - Go back
e - Exit

Enter your desired option: 1
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 ro.debuggable
=====================================

This will set ro.debuggable to:

1

Pick an option below to change
what boot stage the prop will
be set in, or set/reset a delay:

1 - Default (current)
2 - post-fs-data
3 - late_start service
4 - Both boot stages
d - Delay

Do you want to continue?

Enter y(es), n(o), e(xit)
or an option from above: y

Working. Please wait...

Working. Please wait...

Working. Please wait...

Working. Please wait...

Working. Please wait...
```

```bash
MagiskHide Props Config v6.1.2
by Didgeridoohan @ XDA Developers

=====================================
 Reboot - ro.debuggable
=====================================

Reboot for changes to take effect.

Do you want to reboot now (y/n)?

Enter y(es), n(o) or e(xit): y

Rebooting...
```
