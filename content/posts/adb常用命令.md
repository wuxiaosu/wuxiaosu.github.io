---
title: "adb常用命令"
date: 2021-07-14T09:52:34+08:00
draft: false
tags: ["adb","android"]
---
# adb 常用命令

## 1.查看最上层 **Activity** 名字  

+ Linux  

```bash
adb shell dumpsys activity | grep "mResumedActivity"
```

+ Windows  

```bash
adb shell dumpsys activity activities | findstr mResumedActivity
```

## 2.启动组件

+ 启动 **Activity**  

```bash
adb shell am start -n com.google.android.network2/com.my.MainActivity
```

+ 启动 **Service**

```bash
adb shell am startservice -n com.google.android.network2/com.my.MainActivity
```

+ 发送 **Broadcast**

```bash
adb shell am broadcast -a android.intent.action.BOOT_COMPLETED
```

## 3.重启

+ 重启到 **Recovery** 界面  

```bash
adb reboot recovery
```

+ 重启到 **bootloader** 界面

```bash
adb reboot bootloader
```

## 4.其他

+ 强制结束应用

```
adb shell am force-stop <PACKAGE>
```

## 5.以调试模式启动应用

```
adb shell am set-debug-app -w {package_name}
```

清除调试模式
```
adb shell am clear-debug-app
```

## 6.查看应用安装路径

+ 列出所有安装的包

```
adb shell pm list packages -f
```

+ 查看安装包路径
```
adb shell pm path {package_name}
```
+ 查看安装包路径
```
adb shell dumpsys package {package_name} | findstr codePath

adb shell dumpsys package {package_name} | grep codePath
```
+ 卸载系统应用
```
adb shell pm uninstall --user 0 {package_name}
```
