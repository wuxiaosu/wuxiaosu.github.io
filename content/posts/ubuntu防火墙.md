---
title: "ubuntu 防火墙"
date: 2021-03-24T18:34:00+08:00
draft: false
tags: ["Ubuntu"]
---
# ubuntu 防火墙

- 查看防火墙状态

```bash
sudo ufw status
```

- 允许访问端口

```bash
sudo ufw allow 9090/tcp
```

- 禁止访问端口

```bash
sudo ufw deny 9090
```

- 删除规则

```bash
sudo ufw delete deny 9090
```
