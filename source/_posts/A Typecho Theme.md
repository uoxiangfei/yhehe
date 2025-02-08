---
title: A Typecho Theme
date: 2024-01-05 04:29:00
categories: 学习笔记
urlname: 32
tags:
- 学习
---
<!--markdown-->外观设置

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
