---
title: 思源笔记发布工具v0-6-7发布
slug: siyuan-note-release-tool-v067-published-1aluqf
url: /post/siyuan-note-release-tool-v067-published-1aluqf.html
tags:
  - 版本
  - 优化
  - 修复
  - 变更
  - 使用
  - sy-p-067
categories:
  - zh-cn
  - blog
  - releases
lastmod: '2023-01-12 12:07:08'
toc: true
keywords: 版本,优化,修复,变更,使用,sy-p-067
description: >-
  自 v0.6.1 发布之后，我的内心其实是很忐忑的，结果果然发现了一些不能容忍的 bug ，因此，原本计划的终极版本 v0.6.1 也在紧急发布修复版本，到
  v0.6.7​ 版本，才是终于感觉比较满意了。
isCJKLanguage: true
---

## 版本欢迎语

风雨送春归，飞雪迎春到。大家新年好呀，伴随着新年的到来，我们也惊喜的引来了经过细心打磨和优化的 `sy-post-pulisher`​ 的 `v0.6.7`​ 版本。

自 ~~v0.6.1~~ 发布之后，我的内心其实是很忐忑的，结果果然发现了一些不能容忍的 bug ，因此，原本计划的终极版本 ~~v0.6.1~~ 也在紧急发布修复版本，到 `v0.6.7`​ 版本，才是终于感觉比较满意了。

## 核心变更

此版本 `未引入重大需求`​ ，主要核心是进行大幅度的 `使用体验优化`​ 和 `功能优化`​ 。核心优化包括：

* PicGO 体验深度优化
* 更换新的 Xmlrpc 库
* 平台适配（支持发布文章启用图床，增加配置友好的提示，修复 Typecho 的 xmlrpc 可能输出的非法字符等）
* 详情页新增贴心功能按钮
* 局域网文章分享
* 配置问题紧急修复，分享链接修复
* 切换代理

## 项目变更列表

更详细的变更如下：

### 破坏性变更

|修改点|备注|
| -----------------------------------------------| ---------------------------------------------------------------------------------|
|Chrome 插件使用 Metaweblog 相关平台时暂时走代理|新的 Xmlrpc 库在 background.js 解析返回结果的时候反序列化失败，暂时切换为使用代理|

### 问题修复及使用体验优化

|修改点|备注|
| -------------------------------------------------| ---------------------------------------------------------------------------------------------|
|[#309](https://github.com/terwer/src-sy-post-publisher/issues/309) 深度适配 Typecho|移除头部错误信息|
|[#235](https://github.com/terwer/src-sy-post-publisher/issues/235) 支持复制分享链接|Chrome 浏览器插件不处理分享链接，其他情况生成局域网分享链接<br />支持预览页面使用系统默认浏览器打开<br />|
|[#264](https://github.com/terwer/src-sy-post-publisher/issues/264) 虚拟链接转换为真实链接||
|[#304](https://github.com/terwer/src-sy-post-publisher/issues/304) 修复文章图片有备注的时候解析错误||
|[#311](https://github.com/terwer/src-sy-post-publisher/issues/311) Github 系列平台支持单篇文章重新设置 formatter|目前主要仅支持是否生成永久链接、菜单标题，权重字段自定义，HUGO 平台支持修改菜单标题和权重|
|[#315](https://github.com/terwer/src-sy-post-publisher/issues/315) Github 单独生成所有属性需要刷新页面||
|Github 平台支持上传图片到图床||
|Metaweblog 平台适配新的 Xmlrpc 解析库||
|文章预览页面代码块新增 Markdown、php 支持||
|文章预览页面优化 blockquote 样式||
|优化 PicGO 图片列表展示||
|优化 PicGO 图片预览||
|优化 PicGO 路径读取||
|优化体验，非插槽不显示按钮||
|优化按钮，新增图床配置按钮||
|优化按钮图标、操作图标||
|修复本地图片完整链接展示错误的问题||
|修复 Docsy 不显示文档问题||
|修复 Github 平台发布状态 bug||
|修复 md5 依赖库||
|修复平台判断问题||
|修复当前页面未正确显示问题||
|修复思源笔记 2.6.3 版本之后弹出窗口无法关闭的问题||
|修复标签样式错乱问题||
|修复通用 API 请求错误||
|图床列表支持单个图片强制上传覆盖|图床支持单个图片重新上传|
|图床适配公共平台||
|处理数据加载失败的情况||
|导出数据文件名格式改为 sy-p-v-[version].json||
|封装文章图片上传到图床的公共方法||
|忽略不是本地图片的链接||
|提供更友好的 PicGO 错误提示||
|文章列表加入 loading 提升用户体验||
|新增图床全局开关||
|新增链接解析器||
|极致简化简洁模式下的 Github 平台发布操作||
|极致简化简洁模式下的其他平台发布操作||
|浏览器插件设置项增加提示||
|统一代理地址获取||
|美化 Picgo 上传按钮||
|通用平台新增更加友好的提示||
|隐藏浏览器放插件由于限制而无法实现的功能||
|紧急修复 [思源配置读取出错](https://github.com/terwer/src-sy-post-publisher/commit/b3b8ddd5103ec77d9c175f92bcf2a5f3e1e0641e) 问题||
|[局域网文章分享给出提示，因为可能存在伺服未打开的情况](https://github.com/terwer/src-sy-post-publisher/commit/9afa0e68f2d0e4e8521c4b0590cf95e3e093284d)||
|[修复配置保存之后刷新页面错误的问题](https://github.com/terwer/src-sy-post-publisher/commit/6a69cc99cf22fe8faba6a46c722ed9b71a0a82e3)||
|[提取 simple-xmlrpc 为新项目](https://github.com/terwer/src-sy-post-publisher/commit/6b099ebd4d34278a663105f0b19ebd5ecd99ce92)||
|[统一整合设备判断](https://github.com/terwer/src-sy-post-publisher/commit/ddfb467791c8098d27b4332c396c13e21a3efd2e)||
|[切换跨域代理](https://github.com/terwer/src-sy-post-publisher/commit/79f8882872ab8f5feda4729351d79ffbee541e5d)||
|[Metaweblog 平台增加友好提示](https://github.com/terwer/src-sy-post-publisher/commit/9699356aaa4ca8ec4c6ecbc4942e9d40b22d0487)||
|[Metaweblog 平台支持图床](https://github.com/terwer/src-sy-post-publisher/commit/6b1c95d7e70eaff9013aa60e02ff5f5ab368b305)||

### 开发重构

|修改点|备注|
| ----------------------------------| ---------------------------------------------------------------------------------------------------------------------------|
|[#310](https://github.com/terwer/src-sy-post-publisher/issues/310) 更换 xmlrpc 解析库|原来的 xmlrpc 库已经 6 年多不再维护，继续使用有较大风险，使用 @foxglove/xmlrpc 重构之后代替。目前重构版本：[https://github.com/terwer/simple-xmlrpc](https://github.com/terwer/simple-xmlrpc)<br />详情可见 issue：[baalexander/node-xmlrpc#147](https://github.com/baalexander/node-xmlrpc/issues/147)|
|升级 eslint、PicGO-core、vitest 等||
|对 Picgo 组件进行组件化重构||
|提供 PicoGO 配置在线文档|[https://docs.publish.terwer.space/post/picgo-diagram-bed-use-zxqqec.html](https://docs.publish.terwer.space/post/picgo-diagram-bed-use-zxqqec.html)|
|新增文档站，更新文档链接|新文档站请移步：[https://docs.publish.terwer.space](https://docs.publish.terwer.space)|

## 暂时搁置的特性

|修改点|备注|
| --------------------------------| --------------------------------------------|
|下载图片到本地其实不太需要，搁置<br />|<br />|
|废弃发布时候的双链替换|这个应该由展示平台自己去控制，发布工具不处理|

最后，祝大家新年快乐，来年发大财！

‍
