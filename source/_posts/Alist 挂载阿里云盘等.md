---
title: Alist 挂载阿里云盘等
date: 2024-02-23 04:51:00
categories: 学习笔记
headimg: https://yhehe.com/images/2829302099.png
description: Alist是一个支持多种存储的文件列表程序
tags:
- Alist
---


AList 开源项目地址：https://github.com/alist-org/alist

首先我们需要获取到阿里云盘的 refresh_token

傻瓜方法：https://easy-token.cooluc.com/
手动方法：https://youtu.be/12QoxeljMoY?t=445

RaiDrive :
官网：https://www.raidrive.com (免费版即可)
下载好后输入启动命令:alist server
vbs脚本内容
{bs-font color="#9B0B0B"}注意地址写为你的alist文件地址{/bs-font}
```
Set ws = CreateObject("Wscript.Shell")
ws.run "C:\alist-windows-amd64\alist.exe server",vbhide
```