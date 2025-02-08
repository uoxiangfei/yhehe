---
title: hexo 学习记录 #标题
date: 2024-11-06 # 发布时间
tags: 学习,hexo #标签
headimg: https://yhehe.com/images/hexo.png #博客封面图
description: 学习中............
author: hehe  #作者名称
categories: 学习笔记 #分类
updated: 2024-10-10
password: hello
---

### 3. 高亮一段代码[^code]


安装插件
npm i hexo-blog-encrypt -s
git add .
git commit -m a
git push origin main

```js
// 给页面里所有的 DOM 元素添加一个 1px 的描边（outline）;
[].forEach.call($$("*"),function(a){
  a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16);
})
```
{% gallery %}
![图片描述](https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)
{% endgallery %}

创建文章 https://volantis.js.org/v5/page-settings/?keyword=%E6%96%87%E6%A1%A3%E9%A1%B5%E9%9D%A2#%E9%A1%B5%E9%9D%A2%E5%B8%83%E5%B1%80%E6%A8%A1%E6%9D%BF
{% pandown 网盘类型::网盘链接::提取码(可为空)::文件名 %}
{% audio https://github.com/volantis-x/volantis-docs/releases/download/assets/Lumia1020.mp3 %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}



{% link 如何参与项目::http://www.58isp.com/?id=28/::https://photo.yhehe.com/tp/wk.png %}


带 {% u 下划线 %} 的文本；带 {% emp 着重号 %} 的文本；带 {% wavy 波浪线 %} 的文本；带 {% del 删除线 %} 的文本

键盘样式的文本：{% kbd ⌘ %} + {% kbd D %}

密码样式的文本：{% psw 这里没有验证码 %}

各种颜色的标签，包括：{% span red::红色 %}、{% span yellow::黄色 %}、{% span green::绿色 %}、{% span cyan::青色 %}、{% span blue::蓝色 %}、{% span gray::灰色 %}。

超大号文字：

{% span center logo large::Volantis %} {% span center small::A Wonderful Theme for Hexo %}

{% noteblock::标题（可选） %}

Windows 10不是為所有人設計,而是為每個人設計

{% noteblock done %}
嵌套测试： 请坐和放宽，我正在帮你搞定一切...
{% endnoteblock %}

{% folding yellow::Folding 测试： 点击查看更多 %}

{% note warning::不要说我们没有警告过你 %}
{% noteblock bug red %}
我们都有不顺利的时候
{% endnoteblock %}

{% endfolding %}
{% endnoteblock %}

{% checkbox 纯文本测试 %}
{% checkbox checked::支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% checkbox red::支持自定义颜色 %}
{% checkbox green checked::绿色 + 默认选中 %}
{% checkbox yellow checked::黄色 + 默认选中 %}
{% checkbox cyan checked::青色 + 默认选中 %}
{% checkbox blue checked::蓝色 + 默认选中 %}
{% checkbox plus green checked::增加 %}
{% checkbox minus yellow checked::减少 %}
{% checkbox times red checked::叉 %}

{% radio 纯文本测试 %}
{% radio checked::支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% radio red::支持自定义颜色 %}
{% radio green::绿色 %}
{% radio yellow::黄色 %}
{% radio cyan::青色 %}
{% radio blue::蓝色 %}

--------------


{% timeline %}

{% timenode 2020-07-24 [2.6.6 -> 3.0](https://github.com/volantis-x/hexo-theme-volantis/releases) %}

1. 如果有 `hexo-lazyload-image` 插件，需要删除并重新安装最新版本，设置 `lazyload.isSPA: true`。
2. 2.x 版本的 css 和 js 不适用于 3.x 版本，如果使用了 `use_cdn: true` 则需要删除。
3. 2.x 版本的 fancybox 标签在 3.x 版本中被重命名为 gallery 。
4. 2.x 版本的置顶 `top: true` 改为了 `pin: true`，并且同样适用于 `layout: page` 的页面。
5. 如果使用了 `hexo-offline` 插件，建议卸载，3.0 版本默认开启了 pjax 服务。

{% endtimenode %}

{% timenode 2020-05-15 [2.6.3 -> 2.6.6](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.6) %}

不需要额外处理。

{% endtimenode %}

{% timenode 2020-04-20 [2.6.2 -> 2.6.3](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.3) %}

1. 全局搜索 `seotitle` 并替换为 `seo_title`。
2. group 组件的索引规则有变，使用 group 组件的文章内，`group: group_name` 对应的组件名必须是 `group_name`。
2. group 组件的列表名优先显示文章的 `short_title` 其次是 `title`。

{% endtimenode %}

{% endtimeline %}

------------------
不设置任何参数的 {% btn 按钮:: / %} 适合融入段落中。

regular 按钮适合独立于段落之外：

{% btn regular::示例博客::https://xaoxuu.com::fas fa-play-circle %}

large 按钮更具有强调作用，建议搭配 center 使用：

{% btn center large::开始使用::https://volantis.js.org/v3/getting-started/::fas fa-download %}

----------------
{% btns circle grid5 %}
{% cell xaoxuu::https://xaoxuu.com::https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu::https://xaoxuu.com::https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu::https://xaoxuu.com::https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu::https://xaoxuu.com::https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu::https://xaoxuu.com::https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% endbtns %}

-----------
{% btns rounded grid5 %}
{% cell 下载源码::/::fas fa-download %}
{% cell 查看文档::/::fas fa-book-open %}
{% endbtns %}

{% btns circle center grid5 %}
<a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1'>
  <i class='fab fa-apple'></i>
  <b>心率管家</b>
  {% p red::专业版 %}
  <img src='https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_pro.png'>
</a>
<a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1'>
  <i class='fab fa-apple'></i>
  <b>心率管家</b>
  {% p green::免费版 %}
  <img src='https://gcore.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_lite.png'>
</a>
{% endbtns %}


{% sites only:community_team %}

{% menu 下拉菜单 %}
{% menuitem 主题源码::https://github.com/volantis-x/hexo-theme-volantis/::fas fa-file-code %}
{% menuitem 更新日志::https://github.com/volantis-x/hexo-theme-volantis/releases/::fas fa-clipboard-list %}
{% menuitem hr %}
{% submenu 有疑问？::fas fa-question-circle %}
{% menuitem 看 FAQ::/faqs/ %}
{% menuitem 看 本站源码::https://github.com/volantis-x/volantis-docs/ %}
{% menuitem 提 Issue::https://github.com/volantis-x/hexo-theme-volantis/issues/ %}
{% endsubmenu %}
{% endmenu %}


{% menu 这个是::下拉菜单 %}
（同上）
{% endmenu %}

{% menu 这个是::下拉菜单::的示例效果。 %}
（同上）
{% endmenu %}


{% tabs 页面内不重复的ID %}
<!-- tab 栏目1 -->
内容
<!-- endtab -->
<!-- tab 栏目2 -->
内容ee
<!-- endtab -->
{% endtabs %}


{% folding 查看图片测试 %}

![](https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open::查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green::查看代码测试 %}
sss
{% endfolding %}

{% folding yellow::查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red::查看嵌套测试 %}

{% folding blue::查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://gcore.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}


这是 {% inlineimage https://gcore.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %} 一段话。

这又是 {% inlineimage https://gcore.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif::height=40px %} 一段话。


添加描述：

{% image https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg::alt=每天下课回宿舍的路，没有什么故事。 %}

指定宽度：

{% image https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg::width=400px %}

指定宽度并添加描述：

{% image https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg::width=400px::alt=每天下课回宿舍的路，没有什么故事。 %}

设置占位背景色：

{% image https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg::width=400px::bg=#1D0C04::alt=优化不同宽度浏览的观感 %}


{% gallery::::one %}
![图片描述](https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/B18FCBB3-67FD-48CC-B4F3-457BA145F17A.jpeg)
![图片描述](https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/67239FBB-E15D-4F4F-8EE8-0F1C9F3C4E7C.jpeg)
![图片描述](https://gcore.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/00E0F0ED-9F1C-407A-9AA6-545649D919F4.jpeg)
{% endgallery %}


{% pandown baidu::https://baidu.com::1234::百度网盘 %}
{% pandown ty::https://example.com::1234::天翼云 %}
{% pandown aliyun::https://example.com::1234::阿里网盘 %}
{% pandown 123::https://example.com::1234::123网盘 %}
{% pandown qn::https://example.com::1234::七牛云 %}
{% pandown github::https://example.com::::Github %}
{% pandown lz::https://example.com::1234::蓝奏云 %}


{% sites only:test_demo %}