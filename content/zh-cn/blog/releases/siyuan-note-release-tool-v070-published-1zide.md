---
title: 思源笔记发布工具v0-7-0发布
slug: siyuan-note-release-tool-v070-published-1zide
url: /post/siyuan-note-release-tool-v070-published-1zide.html
tags:
  - 配置
  - 支持
  - 发布
  - 设置
  - 操作
  - sy-p-070
categories:
  - zh-cn
  - blog
  - releases
lastmod: '2023-02-28 00:43:01'
toc: true
keywords: 配置,支持,发布,设置,操作,sy-p-070
description: 经过一段时间的重构和优化之后终于和大家见面了。
isCJKLanguage: true
---



经过一段时间的重构和优化之后，0.7.0 终于和大家见面了。

## 下载及安装

思源笔记发布工具的安装步骤如下：

从 `源码仓库 Release 发版页面`​ 、 `Google Chrome 商店`​ 、`Microsoft Edge 商店`​ 下载插件或者在 `思源笔记集市`​ 下载挂件并添加到页面。

[源码仓库 Release 发版页面](https://github.com/terwer/src-sy-post-publisher/releases) <sup>New</sup>

[Google Chrome 商店 - 思源笔记发布工具](https://chrome.google.com/webstore/detail/%E6%80%9D%E6%BA%90%E7%AC%94%E8%AE%B0%E5%8F%91%E5%B8%83%E8%BE%85%E5%8A%A9%E5%B7%A5%E5%85%B7/gemlnnppcphbiimfjnobfgdkohjmgifm?hl=zh-CN) <sup> 已提交，审核中 </sup>

[思源笔记发布工具 - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/aejmkigifflimhjlhjkdckclhabbilee) <sup> 已提交，审核中 </sup>

思源笔记集市：设置 -> 集市 -> 挂件 -> sy-post-publisher <sup> 已发布，等待 D 大合并中 </sup>

## 开始上手

参考：[快速配置](https://docs.publish.terwer.space/docs/getting-started/#%E5%BF%AB%E9%80%9F%E9%85%8D%E7%BD%AE)

## v0.7.0 特性一览 <sup>new</sup>

⚠️ 特别提醒: `0.7.0`​ 为灰度测试版本，所以随时可能发布 `0.7.x`​ 修复版本，请考虑好之后再升级。

### PicGO 相关

* 新增用户友好的 PicGO 图形化配置界面
* 优化 PicGO 配置，支持 PicGO 插件（目前支持水印、s3、minio 三个插件）
* PicGO 默认图床为 github
* PicGO 支持图片重命名
* 云床配置 buffer 读取报错问题，测试常用图床
* PicGO 引入事件监听机制，支持事件注册、事件发布
* PicGO 支持读取多个图床，单个图床支持多份配置

### 系统配置相关

* 整合系统所有配置项，提供统一的配置入口底部的【偏好设置】
* 统一整合导入导出操作位底部的【导入导出】
* 整合【思源 API 地址】设置到【偏好设置】的一个 tab 页
* 整合原通用设置为【个性设置】，操作入口移到【偏好设置】的一个 tab 页

### 发布体验相关

* 【文章绑定】操作非配置项，也是可选功能，放在发布页面容易造成误解，现将操作移入详情页，仅在需要将平台文章与思源笔记建立联系时候使用。新增文章无需操作，新增会自动进行绑定
* 修复浏览器插件不能使用 http，只能用 https 问题
* 修复 typecho 发布文章未成功解析文章 id
* 文章列表图标添加 tooltip
* 插槽按钮添加文字提示
* 新窗口打开时操作按钮 fixed 不随页面滑动

### 开发者相关

* 使用 python 重构项目构建脚本-支持一键打包
* 挂载 SyCmd，适配 Anki 同步（目前仅 Mac 可用）

### 其他

* 修复已知问题，升级部分组件。
