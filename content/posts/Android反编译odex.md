---
title: "Android反编译odex"
date: 2022-05-24T22:06:48+08:00
draft: true
---
## 0.下载 baksmali.jar 、smali.jar  

下载地址
<https://bitbucket.org/JesusFreke/smali/downloads/>  
Github 地址
<https://github.com/JesusFreke/smali>  

## 1. **odex** -> **smali files**  

把手机系统 **/system/framework** 下的内容拷贝到工作目录，和需要转换的 **.odex、.vdex** 文件也拷贝至目录，目录结构如下

```bash
-system
-a.odex
-a.vdex
-baksmali-2.5.2.jar
-smali-2.5.2.jar
```  

然后执行以下命令  

```bash
java -jar baksmali-2.5.2.jar deodex a.odex -b ./system/framework/arm64/boot.oat -o out
```

**-deodex** : 指定 **odex** 文件  
**-b** : 指定 **bootclasspath** 文件  
**-o** : 指定 **smali** 输出目录  

## 2. **smali files** -> **dex**

```bash
java -jar smali-2.5.2.jar assemble out -o a.dex
```

**-assemble** : 指定 **smali files** 文件夹  
**-o** : 指定输出文件名

## 3. 更多

<https://www.cnblogs.com/ysk-china/p/7162203.html?utm_source=itdadao&utm_medium=referral>
