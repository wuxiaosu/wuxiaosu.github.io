---
title: "Frida安装教程"
date: 2021-05-18T10:22:48+08:00
draft: false
tags: ["frida"]
---
Frida是个轻量级的hook框架。

## 安装客户端  

```bash
pip install frida
pip install frida-tools
```

### 查看 frida 版本  

```bash
frida --version
```

出现版本号表示安装成功

## 在 Android 手机中安装服务端  

在手机中查看设备信息

```bash
getprop ro.product.cpu.abi
```

输出结果

```bash
arm64-v8a
```

根据 cpu 版本去官网下载对应的 [frida-server](https://github.com/frida/frida/releases)。

```bash
frida-server-12.8.14-android-arm64.xz
```

将下载并解压后的文件放到设备上

```bash
adb push frida-server-12.8.14-android-arm64 /data/local/tmp
```

端口转发

```bash
adb forward tcp:27042 tcp:27042
```

```bash
adb forward tcp:27043 tcp:27043
```

使用 root 权限运行 frida

```bash
chmod 755 frida-server-12.8.14-android-arm64
```

```bash
./frida-server-12.8.14-android-arm64
```

打开终端，查看 frida-server64 是否运行成功

```bash
frida-ps -U
```

出现设备进程信息表示运行成功。
