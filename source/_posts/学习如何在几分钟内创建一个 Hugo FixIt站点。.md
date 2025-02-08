---
title: 学习如何在几分钟内创建一个 Hugo FixIt站点
date: 2024-07-24 04:17:00
categories: 学习笔记
headimg: https://yhehe.com/images/hugo.png #博客封面图
description: 如果这是您第一次使用Hugo，我们强烈建议你通过这个[适合初学者的优秀文档来了解更多信息。 #章的简短描述，概述文章内容，可以用于SEO优化，帮助搜索引擎和用户快速了解文章主题。
tags:
  - hugo
  - 教程
---


## 先决条件

> 如果这是您第一次使用Hugo，我们强烈建议你通过这个[适合初学者的优秀文档来了解更多信息。](https://gohugo.io/getting-started/)

### 在开始本教程之前，您必须：

[安装 Hugo](https://gohugo.io/getting-started/installing/)（扩展版，v0.127.0或更高版本）
[安装 Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
您还必须能够熟练地使用命令行进行工作。

### 第一种方式

>1.你可以直接在GITHUB 上下载最新的压缩文件，比如：hugo_0.139.2_linux-amd64.tar.gz
2.下载后，上传到服务器的环境变量文件夹下。比如：/usr/local/bin/hugo
3.创建网站文件夹 ，比如:wwwroot/hugo,进入HUGO文件夹后再创建一个存放博客文件的文件夹,输入命令:hugo new site blog
4.进入blog文件夹后执行:先执行git init 再hugo server 如果报错运行一次GIT提交 git add .  git commit -m "Initial commit" 这将使您至少有一个提交记录，Hugo 就能读取 Git 日志了。或者禁用GIT 信息功能，可以在您的配置文件（例如 config.toml）中禁用 Git 信息功能。具体来说，您可以将 enableGitInfo 设置为 false：
5.创建网站：反代http://127.0.0.1:1313 运行目录选择public
6.用 which 命令检查一下 hugo 在不在 PATH 环境变量中。which hugo
7.运行成功后。使用进程守护，将HUGO保持在运行状态。


>查看 hugo 可执行文件的存放位置
>which hugo
>/usr/local/bin/hugo



>验证您是否已安装 Hugo v0.127.0 或更高版本。
```
hugo version
```

###### 启动 Hugo 的开发服务器来查看该站点。
```
hugo server
```

按下Ctrl + C即可停止 Hugo 的开发服务器。

## 添加内容

向您的网站添加新页面。
```
hugo new content posts/my-first-post.md
```
```
Hugo 在content/posts目录中创建了该文件。使用编辑器打开该文件。
```
```
---
title: My First Post
date: 2024-03-01T17:10:04+08:00
draft: true
...
---
```




