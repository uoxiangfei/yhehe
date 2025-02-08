---
title: 利用宝塔面板和PHP实现Typecho定时推送链接到百度
date: 2024-03-01 03:37:00
categories: 学习笔记
headimg: https://yhehe.com/images/1370160430.jpg
description: 网站SEO是一个网站的痛点，虽然没有很好的SEO技术，但是最基础的百度推送还是要做的,这里就是一个实现定时自动推送你网站sitemap到百度的方法，管不管用谁也说不准，但是做了总比不做的好
tags:
  - 宝塔
  - seo
---

网站SEO是一个网站的痛点，虽然没有很好的SEO技术，但是最基础的百度推送还是要做的
这里就是一个实现定时自动推送你网站sitemap到百度的方法，管不管用谁也说不准，但是做了总比不做的好
一、 编写PHP文件
在网站根目录创建一个php文件添加以下内容
```
<?php
header('Content-Type:text/html;charset=utf-8');
$xmldata =file_get_contents("https://自己网站/sitemap.xml");
$xmlstring = simplexml_load_string($xmldata,'SimpleXMLElement',LIBXML_NOCDATA);
$value_array = json_decode(json_encode($xmlstring),true);
$url = [];
for ($i =0;$i < count($value_array['url']);$i++){
    echo $value_array['url'][$i]['loc']."<br/>";
    $url[]= $value_array['url'][$i]['loc'];
}
$api ='百度站长的推送接口';
$ch = curl_init();
$options = array(
   CURLOPT_URL => $api,
   CURLOPT_POST => true,
   CURLOPT_RETURNTRANSFER => true,
   CURLOPT_POSTFIELDS => implode("\n",$url),
   CURLOPT_HTTPHEADER => array('Content-Type:text/plain'),
);
curl_setopt_array($ch, $options);
$result =curl_exec($ch);
echo $result;
 
?>
```
百度站长平台：https://ziyuan.baidu.com/dashboard/index
在百度站长中打开自己的网站（ 注意： 这里的网站一定要跟你推送的网站一致 ）
复制推送接口到上面的代码里，然后在浏览器中访问,出现以下结果说明配置成功
接下来就是定时推送到百度
首先，打开 宝塔面板-计划任务 ，然后添加计划任务
任务类型：访问 URL
任务名称：随意填写
执行周期：随意（建议 6 小时，一天 4 次）
URL 地址：你的域名 / 文件名 .php（例如：https://blog.yhehe.com/baidu.php）