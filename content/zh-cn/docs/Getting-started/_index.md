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
lastmod: '2023-01-08 17:23:07'
toc: true
keywords: 地址,如果,思源,使用,部署,上手,入门
description: 从这里开始一步一步上手使用。
isCJKLanguage: true
weight: 1
---

## 下载及安装

思源笔记发布工具的安装步骤如下：

从 `源码仓库 Release 发版页面`​ 、 `Google Chrome 商店`​ 、`Microsoft Edge 商店`​ 下载插件或者在 `思源笔记集市`​ 下载挂件并添加到页面。

[源码仓库 Release 发版页面](https://github.com/terwer/src-sy-post-publisher/releases)

[Google Chrome 商店 - 思源笔记发布工具](https://chrome.google.com/webstore/detail/%E6%80%9D%E6%BA%90%E7%AC%94%E8%AE%B0%E5%8F%91%E5%B8%83%E8%BE%85%E5%8A%A9%E5%B7%A5%E5%85%B7/gemlnnppcphbiimfjnobfgdkohjmgifm?hl=zh-CN)

[思源笔记发布工具 - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/aejmkigifflimhjlhjkdckclhabbilee)

思源笔记集市：设置 -> 集市 -> 挂件 -> sy-post-publisher

​![](https://img1.terwer.space/api/public/20230108171617.png)​

## 快速配置

### 挂件版挂载菜单打开新窗口操作方式快速上手 <sup> 强烈推荐 </sup>

首先在设置 - 集市 - 挂件 中下载 `sy-post-publisher`​

点击设置 - 外观- 代码片段，代码片段加上下面的 `js`​ 片段，然后重启思源

```js
// 如果不喜欢这个菜单，直接去掉这个代码片段引用即可，去掉之后仍然可以通过挂件版通用方式使用
import("/widgets/sy-post-publisher/lib/siyuanhook.js")
```

点击按钮开始体验

​![](https://img1.terwer.space/api/public/20221228-175950.jpeg)​

详情请参考: [挂件模式用挂载菜单的方式使用](/post/the-pendant-mode-is-used-in-the-method-of-mounting-menu-169wrw.html) <sup> 强烈推荐 </sup> <sup>0.4.2+</sup>

### 浏览器插件方式使用

* 如果本地使用，请确保思源笔记处于打开模式。

  ​![](https://static-rs-terwer.oss-cn-beijing.aliyuncs.com/project/sy-post-publisher/docs/screenshot-20221126-232837.png)​

  如果是 docker 部署，请启动容器。
* 如果本地使用，并且是 `6806`​​ 端口，则 **无需设置** ，请忽略此步骤；

  如果本地使用，但是使用的是随机端口，请在在思源笔记设置-> 关于找到 IP 地址以及端口，然后修改本插件的 `思源 API 地址`​​ ；

  如果是 `远程 docker`​​ 部署，请填写 `外网 API 地址`​​ 以及 `token`​​ ，并配置 `代理地址`​​ 。

  配置地址可在列表页面底部找到：**修改思源 API 地址**

  ​![](https://static-rs-terwer.oss-cn-beijing.aliyuncs.com/project/sy-post-publisher/docs/screenshot-20221126-232612.png)​

  如果您没有支持跨域的代理地址，可以使用我的共享地址：`https://publish.terwer.space/api/middleware`​​ 。出于性能考虑，建议自己部署一份。部署方法请参考 Vercel 远程部署模式 。

* Edge 商店版本打开 popup 默认是文章列表页面；

  挂件模式从 <sup>0.1.0+</sup> 版本开始，会自动检测，如果发现有子文档，会展示文章列表，否则，只展示发布页面。
* 列表页面会有发布预览，新窗口等功能。

  发布页面有设置、国际化、暗黑模式、平台绑定、平台设置、动态平台添加、平台开关等详细功能。后面会逐一讲解。

  初步配置可直接根据提示操作。详细设置请参考后面的文档。

### 思源笔记挂件方式使用

挂件方式使用
首先在设置 - 集市 - 挂件 中下载 `sy-post-publisher`​
然后写好文章
在文中最后面输入 / 找到挂件，选择 `sy-post-publisher`​
然后选择你需要的平台然后进行设置
点击发布即可

### 浏览器直接访问

**打开思源笔记 ​**，并在集市下载 **sy-post-publisher** 挂件，然后 **在浏览器打开** 下面的链接即可直接访问：
[http://127.0.0.1:6806/widgets/sy-post-publisher/blog/?from=siyuan](http://127.0.0.1:6806/widgets/sy-post-publisher/blog/?from=siyuan)

### Vercel 自部署

这个适合有专业技术的人员探索，可参考后续文档。

## 使用

配置完成之后直接点击发布按钮，设置好属性发布即可。高级设置及操作后面会逐一讲解。

‍
