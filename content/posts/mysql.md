---
title: "mysql 相关"
date: 2021-06-18T14:34:00+08:00
draft: false
tags: ["mysql"]
---

+ 开启 mysql 远程访问

确认端口是否对外开放，默认是不开放的

```bash
netstat -an | grep 3306
```

输出如下

```bash
tcp 0   0   127.0.0.1:3306  0.0.0.0:*   LISTEN 
```

修改配置文件（不同版本可能位置不同）

```bash
/etc/mysql/mysql.conf.d/mysqld.cnf
```

注释掉

```bash
# bind-address = 127.0.0.1
```

+ 为新增主键赋值

```sql
SET @mycnt = 0;
UPDATE xxxxx
SET RowNum=(@mycnt := @mycnt + 1)
```

+ 使用 native_password 连接

```sql
ALTER USER 'user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';
```

```sql
flush privileges;
```

+ 修改用户密码

```sql
ALTER USER 'username'@'localhost' IDENTIFIED BY 'new_password';
```

+ 使用默认密码修改数据库密码

查看默认用户密码

```bash
cd /etc/mysql
sudo cat debian.cnf

# Automatically generated for Debian scripts. DO NOT TOUCH!
[client]
host     = localhost
user     = debian-sys-maint
password = G0Gis29yv0dtUhng
socket   = /var/run/mysqld/mysqld.sock
[mysql_upgrade]
host     = localhost
user     = debian-sys-maint
password = G0Gis29yv0dtUhng
socket   = /var/run/mysqld/mysqld.sock
```

使用默认用户登录

```bash
mysql -u debian-sys-maint -p
```

选择 user 表

```bash
use mysql;
```

显示 user 表中的列

```bash
show fields from user;
```

修改密码  

```bash
update mysql.user set authentication_string=password('123456') where user='root';
```

允许远程登录

```bash
grant all on *.* to 'username'@'%' identified by 'password';
FLUSH PRIVILEGES;
```

创建数据库

```bash
create database db;
```

查看所有用户

```bash
select user,host from mysql.user;
```
