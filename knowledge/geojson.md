---
title: GeoJson地理
description: 
published: 1
date: 2025-03-10T14:27:35.387Z
tags: 
editor: markdown
dateCreated: 2025-03-10T14:27:35.387Z
---

# Header
从https://www.gadm.org/ 下载了法国地图 

Level 0-4的级别
用test.py处理数据 去掉crs 并且遵循 相应的规则

GeoJSON 的"右手法则"(Right-hand rule)规范，具体规则是：
外环（outer ring）必须是逆时针方向（counter-clockwise）
内环（inner rings，即孔洞）必须是顺时针方向（clockwise）

并且通过了 https://geojsonlint.com/ 站点的数据校验