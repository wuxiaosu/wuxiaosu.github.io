---
title: "Python文件打包"
date: 2022-05-24T22:06:48+08:00
draft: true
---
## 0.省流助手  

```bash
pyinstaller -F myfile.py
```

## 1.安装 Pyinstaller  

### 1.1 先安装 pywin32  

```bash
pip install pywin32
```

### 1.2 再安装 Pyinstaller  

```bash
pip install PyInstaller
```

## 2.使用 Pyinstaller  

```bash
pyinstaller -F myfile.py
```

### 2.1 输入参数含义

```bash
-F, --onefile 生成单个可执行文件
```

如果一切正常，会在 .py 文件同目录下的 dist 目录生成 .exe 文件  
查看更多参数

```bash
pyinstaller -h
```
