---
title: home
description: 
published: 1
date: 2025-03-09T05:30:09.260Z
tags: 
editor: markdown
dateCreated: 2025-03-09T04:54:30.645Z
---

# Umbogo

## umbogo最新设计

httpserver http
system     系统
ca            授权部分
app          主应用
connect  设备连接管理模块
cache      数据缓存模块
database 数据库模块
message  命令消息传递
support  tts trap snmp 


## umbogo 组网
一种单一的 网络连接方法 已经不能满足当前设备的了
所以 要想办法 适应多种技术
现在已有 
蒲公英 现有 限制很多 3台
wireguard 准备要上了 要测试
zerotier 要继续

还要在安播当中 增加 对于 zeroetier和 wireguard tailscale服务的 检测


## umbogo 待开发
1.新架构 自动化编译
2.升级保存数据 db config
3.接口保存 可编辑
4.反代拆分
5.菜单和用户权限 
6.web 多语言 合并进入 py po文件
vue项目 创建规则
看看有多少_t()
然后用po文件
多语言 法文

7异步请求更换处理 状态并发
8ca看一下 能不能用cron的方式设置定时器 而不是


