---
title: 更详细的pinghsu主题设置教程 
date: 2023-12-18 02:28:00
categories: 学习笔记
urlname: 10
tags:
---
<!--markdown-->这篇教程，属于新手向，请和pingshu主题搭配使用。教程分为三个部分，分别为typecho后台设置，typecho插件使用，pinghsu主题设置
typecho后台设置
基本设置

登录到typecho后台，进入设置-基本设置

站点名称，站点地址是你安装好typecho的一些基本信息，

站点描述和关键词，是你首页的seo信息，得填

pinghsu和lpisme主题都集成了基本的seo功能，对文章页都做了关键字和描述

剩下的就根据你自己的需要去改吧，下图是我的设置

基本设置.png
评论设置

pinghsu和lpisme主题启用Pjax都需要提前关闭开启反垃圾保护，因为这段js会和pjax的js有冲突

另外我们的评论垃圾处理可以通过插件来过滤

其他就根据你的需要去改吧，下图是我的设置

评论设置.png
阅读设置

这部分比较简单，其中每页文章数目是首页文章数目的设置，我是设置为12

其他就根据你的需要去改吧，下图是我的设置

阅读设置.png
永久链接

这部分属于伪静态的内容

我web环境是LNMPA，可以直接用.htaccess去实现伪静态

我的.htaccess为

[object Object],[object Object],[object Object]

如果是LNMP，可以通过修改你站点的nginx的conf配置实现，代码如下

[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object],[object Object]

其他就根据你的需要去改吧，下图是我的设置

永久链接.png
typecho插件使用

之前我写过一篇《目前我在用的一些Typecho插件》

目前我依然也是在使用这些插件

其中我对Typecho缓存插件进行了修改，可以去看我另外一篇《修复TpCache一个无法触发缓存刷新的bug》的最后部分

另外我也通过修改typecho系统让其支持了文章链接添加新窗口跳转，可以看我另外一篇《给Typecho的文章链接添加新窗口跳转》
pinghsu主题设置

这部分在这篇《Pinghsu，A Typecho Theme》里已经写得很详细了

需要注意的是，创建归档页，选择页面模板的时候，还需要填写archive字段

功能开关部分，建议开启的有 Pjax加速，DNS预解析，其他就根据你的需要去启用吧

如果你想获取跟我一样的友情链接页面，因为是typecho开发版，支持在页面内写<ul><li>

所以你可以直接在<ul>内联一个class="flinks",然后在<li>插入你的友链，即可

主题亮点

页面预加载与DNS预解析保证极快访问速度
无JQuery，无前端框架，无webfont
几乎零代码冗余，几乎每句代码都是有意义的
HighlightJS代码高亮，支持22种编程代码
响应式设计，支持平板与手机，访问体验甚至优于桌面
支持图片CDN镜像，支持多种文章缩略图设置
支持首页三栏和单栏选择，文章题图和色块
支持文章目录、相关文章与数学公式渲染
支持文章个性化标徽设置，10种标徽选择
支持个人社交按钮，社交分享
主题设置添加XSS检测，评论提交防止触发多次
还有更多亮点等你去发现~
更多预览

首页 - 三栏	首页 - 单栏
首页-三栏.png	首页-单栏.png
文章内容页 - 题图	文章内容页 - 目录
文章内容页-题图.png	文章内容页-目录.png
页面内容页	内容页 - 评论
页面内容页.png	内容页-评论.png
分类页	模板归档页
分类页.png	模版归档页.png
搜索页	404
搜索页.png	404页.png
移动端 - 首页	移动端 - 文章页	移动端 - 分类页
移动端-首页.png	移动端-内容页.png	移动端-分类页.png
主题使用

到 Github 下载，点击"Download ZIP"下载，解压后将文件夹改名为pinghsu后上传到 /usr/themes，并启用主题

如果需要更新主题，则先下载最新文件，然后覆盖原文件即可完成更新，部分新增加的功能需要到后台开启才会生效

注意事项：目前主题仅在 typecho 开发版，PHP7.0 下测试通过，其他情况未作太多测试

外观设置

外观设置主要分为四部分，分别为 logo、icon 的设置，功能开关，社交按钮设置，图片CDN镜像

使用注意事项都在设置里写得比较清楚了，如果遇到不明白的地方，可以给我留言反馈

下面有几点补充

CDN设置部分仅仅测试了七牛的，理论上也支持有镜像服务的CDN
创建模板归档页，无论选择了哪个模板都要加上自定义字段archive
独立搜索页

设置方法看这里：Here

文章缩略图

文章设置缩略图方法有四种，自定义字段thumb，文章附件第一张图片，文章内图片，默认缩略图

优先级顺序 ：自定义字段 thumb -> 附件第一张图片 -> 文章图片 -> 默认缩略图 -> 随机图片 -> 无

缩略图尺寸大小，高度至少有250px，宽度大于高度，推荐高度为400px的

个性化标徽

个性化标徽出现的地方有首页、分类页，标签页，作者页和相关文章

设置方法是在文章编辑内填写自定义字段，支持的字段如下

book 、 game 、 note 、 chat 、 code 、 image 、 web 、 link 、 design 、 lock

个性化色块

个性化色块需要到外观设置那开启才能激活使用，色块出现的地方有首页，分类页，标签页，独立搜索页等等

设置方法是在文章编辑内填写自定义字段，支持的字段如下

blue、purple、green、yellow、red

友情链接

如果你想获取跟我一样的友情链接页面，因为是 typecho 开发版，支持在页面内写<ul><li>

所以你可以直接在<ul>内联一个class="flinks",然后在<li>插入你的友链，即可

更多设置教程 : Here

浏览器兼容情况

这个····现代浏览器都兼容····

Contributing

All kinds of contributions (enhancements, new features, documentation & code improvements, issues & bugs reporting) are welcome.

欢迎各种形式的贡献，包括但不限于优化，添加功能，文档 & 代码的改进，问题和 bugs 的报告。

License

Open sourced under the MIT license.

根据 MIT 许可证开源。