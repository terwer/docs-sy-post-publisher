---
title: Hugo平台配置指南
slug: hugo-2x5m9a
url: /post/hugo-2x5m9a.html
date: '2022-09-27 10:00:30'
tags:
  - 博客
  - 推荐
  - 安装
  - 准备
  - 工作
  - sy-p-040
categories:
  - zh-cn
  - docs
  - Platform-setting
lastmod: '2023-01-08 18:19:59'
toc: true
keywords: 博客,推荐,安装,准备,工作,sy-p-040
description: 以 HUGO 的 NEXT 主题为例，对 HUGO 平台配置进行说明，其实这也应该是 HUGO 平台的最佳实践之一。
isCJKLanguage: true
---

## HUGO 官网

[The world’s fastest framework for building websites | Hugo (gohugo.io)](https://gohugo.io/)

## 安装 HUGO

```bash
brew install hugo
```

## 准备工作

HUGO 博客部署：这个相信大家都已经会了。不过这里还是推荐一个最佳实践。

推荐使用 [hugo-theme-next-starter](https://github.com/hugo-next/hugo-theme-next-starter) 生成博客。

博客设置参考：[hugo-theme-next](https://github.com/hugo-next/hugo-theme-next#-direct-reference)

```bash
git submodule add https://github.com/hugo-next/hugo-theme-next.git themes/hugo-theme-next
```

我开发此功能的测试博客：[https://hugo.terwer.space](https://hugo.terwer.space)

源码：[https://github.com/terwer/hugo-blog](https://github.com/terwer/hugo-blog)

## HUGO 的 front-matter 规则

[Front Matter | Hugo (gohugo.io)](https://gohugo.io/content-management/front-matter/)

## 发布配置

未完待续
