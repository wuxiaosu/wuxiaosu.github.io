---
title: "JetBrains 重置试用"
date: 2021-02-25T16:30:00+08:00
draft: false
tags: ["jetbrains"]
---
# JetBrains 2020.3 系列通用重置 30 天试用（不会影响其他配置）

## 以 IntelliJIdea 为例

- 删除此目录下所有文件

```bash
C:\Users\Administrator\AppData\Roaming\JetBrains\IntelliJIdea2020.3\eval
```

- 删除 other.xml 文件

```bash
C:\Users\Administrator\AppData\Roaming\JetBrains\IntelliJIdea2020.3\options\other.xml
```

- 删除注册表下所有项

```bash
计算机\HKEY_CURRENT_USER\Software\JavaSoft\Prefs\jetbrains\idea
```

## 其他诸如 DataGrip、PyCharm 类似