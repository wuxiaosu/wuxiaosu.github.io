---
title: "docker 常用操作"
date: 2021-04-28T10:56:00+08:00
draft: false
tags: ["docker"]
---
# docker 常用操作  

- 搜索镜像

```bash
docker search python
```  

- 拉取镜像

```bash
docker pull python:3.7
```  

- 镜像列表

```bash
docker images
```  

- 正在运行的镜像列表

```bash
docker ps
```  

- 使用镜像启动一个容器

```bash
docker run -itd openjdk:8
```  

- 查看所有容器

```bash
docker ps -a
```

- 创建一个镜像

```bash
docker build -t docker_repo ./docker_repo
```

- 启动并直接进入镜像

```bash
docker run -it ubuntu:14.04
```
