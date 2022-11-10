---
title: "反编译Python打包生成的exe文件"
date: 2022-11-10T17:41:48+08:00
draft: false
tags: ["python","反编译","exe"]
---
## 1.解压 exe 文件  

### 1.1 下载 pyinstxtractor  

<https://github.com/extremecoders-re/pyinstxtractor>

### 1.2 执行解压操作  

```bash
python pyinstxtractor.py <filename>
```

执行成功会出现一个 filename_extracted 目录,目录里面有相对应的 pyc 文件

## 2.反编译 pyc 文件  

### 2.1 安装 uncompyle6

```bash
pip install uncompyle6
```

### 2.1 反编译 pyc 文件

```bash
uncompyle6 xx.pyc 
```  

执行成功即可看到可运行的 python 源码
