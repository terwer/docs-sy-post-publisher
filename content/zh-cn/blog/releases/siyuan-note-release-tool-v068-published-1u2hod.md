---
title: 思源笔记发布工具v0-6-8发布
slug: siyuan-note-release-tool-v068-published-1u2hod
url: /post/siyuan-note-release-tool-v068-published-1u2hod.html
tags:
  - 思源
  - 笔记
  - 发布
  - 工具
  - 版本
  - sy-p-068
categories:
  - zh-cn
  - blog
  - releases
lastmod: '2023-01-30 21:44:51'
toc: true
keywords: 思源,笔记,发布,工具,版本,sy-p-068
description: 此版本主要解决 思源笔记 2.6.3+ 版本 Localstorage 的修改以及随机端口导致的重启无法读取配置问题。
isCJKLanguage: true
---



## 版本说明

在众多小伙伴离乡返岗之际，我们也迎来了 2023 年的第一个小版本 0.6.8，此版本主要解决 思源笔记 2.6.3+ 版本 Localstorage 的修改以及随机端口导致的重启无法读取配置问题。

## 新特性一览

* 提供通用的集成接口，方便思源笔记主题集成本插件

  为了和 `思源笔记主题`​ 更好的集成，`0.6.8+`​ 新增了通用的接口，只需两步即可集成，后续无缝更新，无需调整。步骤如下：

  步骤：
  1、初始化

  ```js
  // 初始化发布辅助功能
  const publishHelperLibPath = `${window.siyuan.config.system.dataDir}/widgets/sy-post-publisher/lib/siyuan/publish-helper.js`
  console.log(
    "自定义js片段将要从以下位置引入发布辅助功能",
    publishHelperLibPath
  )
  const initPublishHelper = window.require(publishHelperLibPath)
  initPublishHelper()
  ```

  2、打开页面

  ```js
  // 参数示例
  // pageid: 20230130095036-7jfvjm0
  // pageUrl:index.html
  window.terwer.renderPublishHelper(pageId, pageUrl)
  ```

  参考：[https://github.com/terwer/src-sy-post-publisher/issues/338](https://github.com/terwer/src-sy-post-publisher/issues/338)
* 重构数据存储方案，思源笔记内部使用 JSON 存储，解决多空间随机端口问题

  在思源笔记内部，即有 `Eletron`​ 环境的情况下使用 JSON 存储数据，其他情况下沿用旧的浏览器 `Localstorage`​ 存储。此重构不涉及功能，导入导出以及其他功能均不受任何影响。

## 下载及安装

思源笔记发布工具的安装步骤如下：

从 `源码仓库 Release 发版页面`​ 、 `Google Chrome 商店`​ 、`Microsoft Edge 商店`​ 下载插件或者在 `思源笔记集市`​ 下载挂件并添加到页面。

[源码仓库 Release 发版页面](https://github.com/terwer/src-sy-post-publisher/releases) <sup>New</sup>

[Google Chrome 商店 - 思源笔记发布工具](https://chrome.google.com/webstore/detail/%E6%80%9D%E6%BA%90%E7%AC%94%E8%AE%B0%E5%8F%91%E5%B8%83%E8%BE%85%E5%8A%A9%E5%B7%A5%E5%85%B7/gemlnnppcphbiimfjnobfgdkohjmgifm?hl=zh-CN) <sup> 已发布 </sup>

[思源笔记发布工具 - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/aejmkigifflimhjlhjkdckclhabbilee) <sup> 已发布 </sup>

思源笔记集市：设置 -> 集市 -> 挂件 -> sy-post-publisher <sup> 已发布 </sup>

## 开始上手

参考：[快速配置](https://docs.publish.terwer.space/docs/getting-started/#%E5%BF%AB%E9%80%9F%E9%85%8D%E7%BD%AE)
