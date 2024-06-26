---
title: "docker 常用操作"
date: 2021-04-28T10:56:00+08:00
draft: false
tags: ["docker","docker compose"]
---
## docker 常用操作  

- 搜索镜像

```bash
docker search python
```  

- 拉取镜像

```bash
docker pull python:3.7
```  

- 查看所有镜像

```bash
docker images
```  

- 删除镜像

```bash
docker rmi
```  

- 正在运行的镜像列表

```bash
docker ps
```  

- 使用镜像启动一个容器

```bash
docker run -itd openjdk:8
```  

- 启动并直接进入镜像

```bash
docker run -it ubuntu:14.04
```

- 查看所有容器

```bash
docker ps -a
```

- 删除容器  

```bash
docker rm
```

- 使用 Dockerfile 构建镜像

```bash
docker build -t docker_repo ./docker_repo
```

- 查看容器状态  

```bash
docker stats
```

- 查看日志

```bash
docker compose logs
```

- 后台启动

```bash
docker compose up -d
```

- 启动

```bash
docker compose up
```

- 重启

```bash
docker compose restart
```
