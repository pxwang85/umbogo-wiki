---
title: 教程
description: 
published: 1
date: 2025-03-12T12:04:56.973Z
tags: 
editor: markdown
dateCreated: 2025-03-09T11:29:09.303Z
---

# 配置文件
Your content here

# 添加设备
- [扫描添加设备 *自动扫描设备.*](/instruction/guide/page_device/scan)
- [手动添加设备 *界面操作方式的设想.*](/instruction/design/ui)
{.links-list}

SNMP： 
    现阶段只支持对于PBI私有协议的设备扫描，也暂时没计划对其他设备做支持
    对输入网段的IP地址。 2-255的地址 轮流查询
HTTP： 
    对于2-255地址轮流查询80端口
    主要用于网段内不支持设备的查询，无法知道设备类型
    
HTTP&SNMP：
    组合查询，先找到网段内开80端口的设备，然后再用snmp方法。能够快速找到网络内PBI设备

# 配置报警

## 配置Web数据报警
## 配置Trap报警


