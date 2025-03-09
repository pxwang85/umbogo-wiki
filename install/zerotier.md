---
title: 私有化Zerotier安装
description: 
published: 1
date: 2024-12-11T01:14:08.180Z
tags: 
editor: markdown
dateCreated: 2024-12-10T03:23:00.838Z
---


现在使用 阿里云搭建了一套 私有的Zerotier Plant节点服务
用于解决官方Zerotier连接不稳定的情况, 而且也不受Zerotier免费的各种显示

下载planet文件：可通过浏览器访问http://IPaddress:3180或通过服务器./ztncui/etc/myfs目录获取
[planet](/src/zerotier/planet)

# windows

## 1. 配置planet
替换planet：将下载的planet替换C:\ProgramData\ZeroTier\One\目录下的planet
重启服务：系统搜索 "服务" 然后找到"ZeroTier One"点 重启动 即可
![zerotier_win.png](/src/zerotier/zerotier_win.png)



# linux
## 1. 配置planet
替换planet：将下载的planet替换/var/lib/zerotier-one目录下的planet
重启服务：
```
service zerotier-one restart
```

## 2. 基本命令
### 2.1 安装
```
curl -s https://install.zerotier.com | sudo bash
```

### 2.2 网络加入
```
zerotier-cli join <你的网络ID>
sudo zerotier-cli join network_ID
```

### 2.3 网络离开
```
sudo zerotier-cli leave network_ID
```

### 2.4 网络列表
```
sudo zerotier-cli listnetworks
```

### 2.5 系统服务
```
sudo systemctl start zerotier-one
sudo systemctl enable zerotier-one
sudo systemctl start zerotier-one.service
sudo systemctl enable zerotier-one.service
```

