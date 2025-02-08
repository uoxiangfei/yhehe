---
title: Typecho Plyr HTML5 自适应本地 mp3/mp4 播放插件
date: 2024-03-14 02:20:00
categories: 学习笔记
headimg: https://yhehe.com/images/1354968797.jpg #博客封面图
description: Plyr简单，轻便，可访问且可自定义的HTML5，YouTube和Vimeo媒体播放器，支持现代浏览器。
tags:
  - 软件
---

Plyr简单，轻便，可访问且可自定义的HTML5，YouTube和Vimeo媒体播放器，支持现代浏览器。

更多详情请访问 plyr 官网：https://plyr.io

请参考开源项目自行添加标签：https://plyr.io

既然官方提供了 MP3 播放源码，就一起集成了 MP3 音频播放和 MP4 视频播放功能，整合了其它控件元素，基本上保持与 Plyr 官网样式同步。

使用 Plyr HTML5 样式：

MP3 和移动端效果不提供预览，我自己测试时效果很棒，您可自行测试。

是不是马上觉得使用 Plyr HTML5 样式好看多了？如果您喜欢，就往下看吧。

功能：
PC 端与手机端自适应。
与 Plyr 官方控件样式同步。
只需一个插件，即可播放MP3/MP4。

使用：
MP4：
	`<video src="https://xxx.com/xxx.mp4"></video>`
	
带封面：
	`<video poster="https://xxx.com/xxx.jpg" src="https://xxx.com/xxx.mp4"></video>`
MP3:
	`<div><audio src="http://xxx.com/xxx.mp3"></audio></div>`
	
注：此插件已集成 HTML 5 基本按钮元素控件，无需像原生 HTML 5 一样还要写入元素控件，只需一个视频地址即可播放。

由于设置了不自动播放，想设置MP3自动播放的，请添加自动播放 autoplay 标签或者修改源码 autoplay 标签。

目前仅在 Typecho1.0 测试OK，理论支持所有正式版与开发版，并没有加入 Youtube 与优酷、腾讯等在线视频功能，Youtube 被屏蔽，腾讯和优酷视频都有广告，只测试了本地视频播放，如您有兴趣，也可自己加入测试。

由于我设置了自适应，就不需要添加宽高元素了，如与原生元素发生冲突，保留带封面元素再删除其它元素控件，如果还需要添加其他的元素控件，请参考：https://github.com/sampotts/plyr

插件下载：[plyr.zip](https://yhehe.com/usr/uploads/2024/03/1655393404.zip)

下载之后自行上传到 Typecho 插件目录修改插件名为：plyr 并启用。
