---
title: Rufus U盘工具，重装系统不再烦恼
date: 2024-04-06 04:01:00
categories: 学习笔记
headimg: https://yhehe.com/images/4202432307.jpg #博客封面图
description: Rufus 是一个可以帮助格式化和创建可引导USB闪存盘的工具，比如 USB 随身碟，记忆棒等等。在如下场景中会非常有用：你需要把一些可引导的ISO格式的镜像（Windows，Linux，UEFI等）创建成USB安装盘的时候,你需要使用一个还没有安装操作系统的设备的时候,你需要从DOS系统刷写BIOS或者其他固件的时候,你需要运行一个非常底层的工具的时候
tags:
- 软件
---

Rufus 是一个可以帮助格式化和创建可引导USB闪存盘的工具，比如 USB 随身碟，记忆棒等等。

在如下场景中会非常有用：

你需要把一些可引导的ISO格式的镜像（Windows，Linux，UEFI等）创建成USB安装盘的时候
你需要使用一个还没有安装操作系统的设备的时候
你需要从DOS系统刷写BIOS或者其他固件的时候
你需要运行一个非常底层的工具的时候
 

Rufus 麻雀虽小，五脏俱全，体积虽小，功能全面。

哦，对了，Rufus 还 非常快，比如，在从ISO镜像创建 Windows 7 USB安装盘的时候，他比 UNetbootin，Universal USB Installer 或者 Windows 7 USB download tool 大约快2倍。当然，在创建 Linux 可引导USB设备的时候也比较快。

官网地址：https://rufus.ie

### 系统需求：
需要Windows 7以上的操作系统，无所谓32位还是64位，下载后开箱即用。



### 用法
下载可执行文件后直接运行 – 无需安装，绿色环保

可执行文件已经进行数字签名，详情如下：

“Akeo Consulting” (v1.3.0 或者更新的版本)
“Pete Batard – Open Source Developer” (v1.2.0 或者更老的版本)
 

### 对DOS支持的说明：
如果你创建了一个DOS启动盘，但是没有使用美式键盘，Rufus 会尝试根据设备选择一个键盘布局，在那种情况下推荐使用 FreeDOS（默认选项）而不是 MS-DOS，因为前者支持更多的键盘布局。

### 对ISO支持的说明：
Rufus v1.10 及其以后的所有版本都支持从 ISO 镜像 (.iso) 创建可引导USB。

通过使用类似 InfraRecorder 或者 CDBurnerXP 之类的免费CD镜像烧录程序，可以非常方便的从实体光盘或者一系列文件中创建 ISO 镜像。