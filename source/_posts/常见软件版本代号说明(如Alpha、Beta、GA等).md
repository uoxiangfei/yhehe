---
title: 常见软件版本代号说明(如Alpha、Beta、GA等)
date: 2024-01-22 13:01:00
categories: 学习笔记
headimg: https://bu.dusays.com/2024/02/12/65c9cb930e75a.png
description: 内部测试版本 (Alpha Releases) ，会引入新的功能和改进。Alpha 版是当前系列版本的最初版本。Alpha 版可能存在一些 bug，提供给尝鲜用户，可以用于测试最新的功能。
tags:
- 版本号
---
### Alpha
内部测试版本 (Alpha Releases) ，会引入新的功能和改进。Alpha 版是当前系列版本的最初版本。Alpha 版可能存在一些 bug，提供给尝鲜用户，可以用于测试最新的功能1。
>示例： 1.1 Alpha
### Beta
公开测试版本 (Beta Releases) ，会引入新的功能和改进，相对于内部测试版本已有了很大的改进，消除了严重的错误，但还是存在着一些 bug，提供给尝鲜用户，可以用于测试最新的功能。
> 示例：1.1 Beta
### RC
候选发布版本 (Release Candidate Releases, RC) ，会引入新的功能和改进。RC 版本可用于早期测试，较公开测试版本的稳定性有较大改善，其稳定性足以开始测试，但不适合用于生产部署。
> 示例：
RC1
2.0-RC1
### GA
正式发布版本 (General Availability Releases, GA) ，是当前系列版本的稳定版本，在候选发布版本 (Release Candidate Releases, RC) 之后发布，能够用于生产部署。
> 示例：
1.0 GA
### 纯数字版本号
无代号的纯数字版本号，通常理解为正式版本，同GA
> 示例：
1.0.0
2.0
### DMR
开发里程碑版本 (Development Milestone Releases, DMR) ，通常理解为开发版，新功能尝鲜版本
> 示例：TiDB 6.3.0-DMR
### LTS
长期支持版本 (Long-Term Support Releases, LTS) ，通常理解为稳定版，可长期使用，不会有大功能变更，只修复bug和漏洞。大多数商业软件都提供长期支持版本，如Windows、Ubuntu、Node Js等
> 
示例：
Node 18.12.0 LTS
Ubuntu 22.04.1 LTS