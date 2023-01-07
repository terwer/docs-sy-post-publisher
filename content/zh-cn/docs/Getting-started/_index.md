---
title: 开始上手
slug: start-to-get-started-zi0eyk
date: '2022-09-27 09:49:26'
tags:
  - 地址
  - 如果
  - 思源
  - 使用
  - 部署
  - 上手
  - 入门
categories:
  - zh-cn
  - docs
  - Getting-started
lastmod: '2023-01-08 01:54:21'
toc: true
keywords: 地址,如果,思源,使用,部署,上手,入门
description: 从这里开始一步一步上手使用。
isCJKLanguage: true
linkTitle: 开始上手
weight: 1
---

## 安装

思源笔记发布工具的安装步骤如下  
从 Edge 商店下载插件或者在思源笔记集市下载挂件并添加到页面。  
[思源笔记发布工具 - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/aejmkigifflimhjlhjkdckclhabbilee)

## 快速配置

### 浏览器插件方式使用 <sup> 推荐 </sup>

* 如果本地使用，请确保思源笔记处于打开模式。  

  ​![](https://static-rs-terwer.oss-cn-beijing.aliyuncs.com/project/sy-post-publisher/docs/screenshot-20221126-232837.png)​

  如果是 docker 部署，请启动容器。
* 如果本地使用，并且是 `6806`​​ 端口，则 **无需设置** ，请忽略此步骤；

  如果本地使用，但是使用的是随机端口，请在在思源笔记设置-> 关于找到 IP 地址以及端口，然后修改本插件的 `思源 API 地址`​​ ；

  如果是 `远程 docker`​​ 部署，请填写 `外网 API 地址`​​ 以及 `token`​​ ，并配置 `代理地址`​​ 。

  配置地址可在列表页面底部找到：**修改思源API地址**

  ​![](https://static-rs-terwer.oss-cn-beijing.aliyuncs.com/project/sy-post-publisher/docs/screenshot-20221126-232612.png)​

  如果您没有支持跨域的代理地址，可以使用我的共享地址：`https://publish.terwer.space/api/middleware`​​ 。出于性能考虑，建议自己部署一份。部署方法请参考 Vercel 远程部署模式 。

* Edge 商店版本打开 popup 默认是文章列表页面；

  挂件模式从 <sup>0.1.0+</sup> 版本开始，会自动检测，如果发现有子文档，会展示文章列表，否则，只展示发布页面。
* 列表页面会有发布预览，新窗口等功能。

  发布页面有设置、国际化、暗黑模式、平台绑定、平台设置、动态平台添加、平台开关等详细功能。后面会逐一讲解。

  初步配置可直接根据提示操作。详细设置请参考后面的文档。

### 思源笔记挂件方式使用

挂件方式使用  
首先在设置 - 集市 - 挂件 中下载 sy-post-publisher  
然后写好文章  
在文中最后面输入 / 找到挂件，选择 sy-post-publisher  
然后选择你需要的平台然后进行设置  
点击发布即可

### 浏览器直接访问

**打开思源笔记 ​**，并在集市下载 **sy-post-publisher** 挂件，然后 **在浏览器打开** 下面的链接即可直接访问：  
[http://127.0.0.1:6806/widgets/sy-post-publisher/blog/?from=siyuan](http://127.0.0.1:6806/widgets/sy-post-publisher/blog/?from=siyuan)

## 使用

配置完成之后直接点击发布按钮，设置好属性发布即可。高级设置及操作后面会逐一讲解。