---
title: "Frida Android平台安装教程"
date: 2021-05-18T10:22:48+08:00
draft: false
tags: ["frida"]
---
Frida是个支持多平台的hook框架。

Frida 官网 <https://frida.re/>

下面是Android平台的简单安装教程。

## 在电脑上安装客户端  

```bash
pip install frida-tools
```

### 查看 frida 版本  

```bash
frida --version
```

出现版本号表示安装成功

## 在 Android 手机中安装服务端  

在手机终端执行命令，查看设备信息

```bash
adb shell getprop ro.product.cpu.abi
```

输出设备架构信息

```bash
arm64-v8a
```

根据 cpu 架构去官网下载对应的 [frida-server](https://github.com/frida/frida/releases)。

```bash
frida-server-12.8.14-android-arm64.xz
```

注意 .xz 是压缩文件，需要先解压，然后解压后的文件放到设备上

```bash
adb push frida-server-12.8.14-android-arm64 /data/local/tmp
```

电脑上设置端口转发

```bash
adb forward tcp:27042 tcp:27042
```

```bash
adb forward tcp:27043 tcp:27043
```

在 Android 终端使用 root 权限运行 frida-server

```bash
chmod 755 /data/local/tmp/frida-server-12.8.14-android-arm64
```

```bash
./data/local/tmp/frida-server-12.8.14-android-arm64
```

### 查看 frida-server 是否运行成功

```bash
frida-ps -U
```

出现 Android 设备进程信息表示运行成功。
