---
title: "sqlite常用操作"
date: 2022-01-07T13:46:00+08:00
draft: false
tags: ["sql","sqlite"]
---
# sql

## sqlite

### 时间戳转日期

```sql
select datetime(1613714753, 'unixepoch', 'localtime');
```

输出

```sql
2021-02-19 14:05:53
```

### 当前时间戳

```sql
select strftime('%s','now');
```

输出

```sql
1613714753
```

### 查询所有表  

```sql
SELECT * FROM sqlite_master
```
