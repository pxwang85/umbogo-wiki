---
title: 安播 Windows安装
description: 
published: 1
date: 2025-03-10T22:23:54.699Z
tags: 
editor: markdown
dateCreated: 2025-03-09T05:15:13.915Z
---

# windows安装
系统环境,使用 python3.10开发，不支持windows7系统，windows10,windows11经测试可以使用。


安播使用postgresql数据库作为数据存储，使用influxdb时序性数据库作为状态数据的保存。

安装环境
## 1. Postgresql下载
官网地址：https://get.enterprisedb.com/postgresql/postgresql-14.15-1-windows-x64.exe


## 2. postgresql配置
### 2.1 安装路径
![1.png](/image/postgresql/1.png)

### 2.2 安装选择
![2.png](/postgresql/2.png)

### 2.3 数据存储路径
![3.png](/postgresql/3.png)

### 2.4 修改密码
![4.png](/postgresql/4.png)

### 2.5 配置端口
![5.png](/postgresql/5.png)

### 2.6 语言 
![6.png](/postgresql/6.png)
特别注意，不要修改使用Default Locale

## 3 创建安播用数据库 pms
多种创建数据库的方式 选一种就可以
将来会做到程序里，判断是否存在，如果不存在自动创建

### 方式一 使用postgresql自带PgAdmin4
连接数据库，填写安装数据库时的 数据库密码
![8.png](/postgresql/8.png)

创建数据库database  数据库pms
![9.png](/postgresql/9.png)

如果PgAdmin系统不能用

### 方式二 使用Navicat创建数据库


### 方式三 使用命令行的方式 创建数据库
cd "C:\Program Files\PostgreSQL\{version}\bin"

创建数据库
方式一
```
createdb -U postgres pms
```

方式二
```
psql -U postgres
CREATE DATABASE pms;
```

修改 密码

方式一
```
psql -U postgres -c "ALTER USER postgres WITH PASSWORD 'new_password';"
```

方式二
```
psql -U postgres
\password postgres
```


## 4. Influxdb下载
官网地址： https://docs.influxdata.com/influxdb/v2/install/?t=Windows#download-and-install-influxdb-v2

cmd终端进入对应路径后，执行influxdb
创建账号,密码,组织,仓库后 获取Token


## 5. 安播配置
修改config文件夹下  config.yaml文件
![10.png](/postgresql/10.png)

修改晚配置之后,执行pms


## 6. 配置influxdb

