---
title: 思源笔记发布工具v0-8-0发布
slug: siyuan-note-release-tool-v080-published-z13fdjr
url: /post/siyuan-note-release-tool-v080-published-z13fdjr.html
tags:
  - 发布
  - 思源
  - 笔记
  - 工具
  - 修复
  - sy-p-080
categories:
  - zh-cn
  - blog
  - releases
lastmod: '2023-03-26 12:45:07'
toc: true
keywords: 发布,思源,笔记,工具,修复,sy-p-080
description: 思源笔记发布工具​低调上线。
isCJKLanguage: true
---



思源笔记发布工具 `0.8.0`​ 低调上线。

## 下载及安装

思源笔记发布工具的安装步骤如下：

从 `源码仓库 Release 发版页面`​ 、 `Google Chrome 商店`​ 、`Microsoft Edge 商店`​ 下载插件或者在 `思源笔记集市`​ 下载挂件并添加到页面。

[源码仓库 Release 发版页面](https://github.com/terwer/src-sy-post-publisher/releases) <sup>New</sup>

[Google Chrome 商店 - 思源笔记发布工具](https://chrome.google.com/webstore/detail/%E6%80%9D%E6%BA%90%E7%AC%94%E8%AE%B0%E5%8F%91%E5%B8%83%E8%BE%85%E5%8A%A9%E5%B7%A5%E5%85%B7/gemlnnppcphbiimfjnobfgdkohjmgifm?hl=zh-CN) <sup> 已提交，审核中 </sup>

[思源笔记发布工具 - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/aejmkigifflimhjlhjkdckclhabbilee) <sup> 已提交，审核中 </sup>

思源笔记集市：设置 -> 集市 -> 挂件 -> sy-post-publisher <sup> 已发布，等待 D 大合并中 </sup>

## 开始上手

参考：[快速配置](https://docs.publish.terwer.space/docs/getting-started/#%E5%BF%AB%E9%80%9F%E9%85%8D%E7%BD%AE)

## v0.8.0 特性一览 <sup>new</sup>

### Bug 修复

* 修复普通挂件版使用方式 WordPress 和博客园发布文章报错问题
* 修复图片有备注时无法上传问题，现在支持显示备注为图片的 alt
* 修复 PicGo 设置中的时间戳重命名关闭后会自动打开的问题
* #434 文章没有图片时候图床错误文章发布失败

### 新特性

* 发布至语雀支持笔记间的内部链接替换
* 博客园、WordPress、Typecho 平台支持笔记间的内部链接替换
* Github 平台（HUGO、Hexo、Vitepress 等）支持笔记间的内部链接替换
* 普通挂件版使用方式支持使用图床[受限于 Electron 机制，主窗口直接上传会导致内核崩溃，目前仅支持链接替换，上传仍需打开新窗口]

### 开发重构

* 移除不必要的日志打印
* #420 ankisiyuan.bin（仅支持 Mac） 默认不提供，手动下载，减小打包体积
* 鉴于主窗口直接上传会导致内核崩溃，主窗口移除 PicGO 支持，仅支持新窗口模式使用 PicGO

## 注意事项

1. 图片标题可能部分 Markdown 解析器不支持，但是拖备注和链接大部分平台都可用
2. 双链替换需要设置为锚文本链方式，即生成 siyuan://bkock，另外平台设置的平台首页、预览规则也要对。这样就能自动替换成平台专属地址
