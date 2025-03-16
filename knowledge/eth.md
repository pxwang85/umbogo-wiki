---
title: 网卡名称
description: 
published: 1
date: 2025-03-16T02:04:57.058Z
tags: 
editor: markdown
dateCreated: 2025-03-16T02:04:57.058Z
---

# Header
在Linux系统中，网卡名称的命名规则可以帮助你识别设备类型。以下是一些常见的命名规则：

1. **以太网接口（有线网卡）**：
   - `ethX`：传统命名方式，`X` 是数字，例如 `eth0`, `eth1`。
   - `enpXsY`：现代命名方式，`X` 和 `Y` 是数字，例如 `enp0s3`。`en` 表示以太网，`p` 表示PCI总线，`s` 表示插槽编号。

2. **无线网卡**：
   - `wlanX`：传统命名方式，`X` 是数字，例如 `wlan0`, `wlan1`。
   - `wlpXsY`：现代命名方式，`X` 和 `Y` 是数字，例如 `wlp2s0`。`wl` 表示无线，`p` 表示PCI总线，`s` 表示插槽编号。

3. **USB网卡**：
   - `enxXXXXXXXXXXXX`：USB以太网卡，`X` 是MAC地址的十六进制表示，例如 `enx78e7d1ea46da`。
   - `wlxXXXXXXXXXXXX`：USB无线网卡，`X` 是MAC地址的十六进制表示，例如 `wlx00c0ca8e5e5e`。

这些命名规则可以帮助你快速识别网卡类型。你可以通过以下命令查看系统中的网卡名称及其详细信息：

```bash
ip link show
```

或者：

```bash
ls /sys/class/net
```

这些命令会列出所有网络接口及其名称。


在Linux系统中，你可以通过多种方式获取网卡的硬件信息。以下是几种常用的方法：

### 方法一：使用 `lshw` 命令
`lshw` 是一个强大的硬件信息查看工具，可以显示详细的硬件信息。你可以使用以下命令来获取网卡的信息：

```bash
sudo lshw -class network
```

### 方法二：使用 `ethtool` 命令
`ethtool` 是一个用于查询和控制网卡参数的命令行工具。你可以使用以下命令来获取网卡的信息：

```bash
sudo ethtool -i eth0
```

将 `eth0` 替换为你要查询的网卡名称。

### 方法三：使用 `ifconfig` 或 `ip` 命令
你可以使用 `ifconfig` 或 `ip` 命令来查看网卡的基本信息：

```bash
ifconfig -a
```

或者：

```bash
ip link show
```

### 方法四：使用 `dmidecode` 命令
`dmidecode` 可以显示系统硬件信息，包括网卡信息。你可以使用以下命令来获取网卡的信息：

```bash
sudo dmidecode -t 10
```

### 方法五：使用 `lspci` 命令
`lspci` 可以列出所有PCI设备，包括网卡。你可以使用以下命令来获取网卡的信息：

```bash
lspci | grep -i ethernet
```

如果你需要将这些信息保存到文件中，可以创建一个Shell脚本来实现。以下是一个示例脚本：

### [GetNetworkAdapterInfo.sh](file:///c%3A/Users/pxwang/Desktop/collect/GetNetworkAdapterInfo.sh)

这个脚本将获取所有网络适配器的信息并保存到一个文本文件中。

```bash
#!/bin/bash

# 获取所有网络适配器的信息
network_info=$(sudo lshw -class network)

# 将信息保存到文件中
echo "$network_info" > /c:/Users/pxwang/Desktop/collect/NetworkAdapterInfo.txt
```

运行这个脚本后，你可以在 `/c:/Users/pxwang/Desktop/collect/NetworkAdapterInfo.txt` 文件中查看所有网络适配器的详细信息。

Made changes.