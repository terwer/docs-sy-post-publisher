---
title: 源码编译及项目结构说明
weight: 2
slug: source-code-compilation-and-project-structure-description-2odeob
url: /post/source-code-compilation-and-project-structure-description-2odeob.html
tags:
  - 文件
  - 统一
  - 脚本
  - 源码
  - 编译
categories:
  - zh-cn
  - docs
lastmod: '2023-01-08 02:41:06'
toc: true
keywords: 文件,统一,脚本,源码,编译
description: >-
  项目结构说明与源码编译指南。
isCJKLanguage: true
---

## 项目结构说明

```plantuml
@startmindmap

skinparam backgroundcolor transparent

!include https://static-rs-terwer.oss-cn-beijing.aliyuncs.com/lib/uml/starter-skin.puml

* sy-post-publisher
	* api/ 提供统一的需要server环境的API请求代理
	* assets/ 资源文件、样式文件等
	* components/ 通用组件
	* composables/ 可复用单元
	* layouts/ 页面布局
	* locals/ 国际化
	* pages/ 页面统一出口
	* plugins/ 插件
	* scripts/ 脚本（构建脚本、打包脚本等）
	* stores/ 存储
	* test/ 基于vitest的单元测试
	* typings/ 类型定义文件（主要用于开发阶段的代码智能提示）
	* utils/ 工具类
	* vite.config.ts 统一配置文件
	* vercel.json vercel部署描述文件

@endmindmap
```

如果图片不能查看，请看这里：

​![](https://img1.terwer.space/api/public/20230108023216.png)​

准备

## 源码编译

通过源码编译：  
[https://github.com/terwer/src-sy-post-publisher](https://github.com/terwer/src-sy-post-publisher)

```bash
git clone https://github.com/terwer/src-sy-post-publisher
```

```bash
npm i -g pnpm
npm i -g vercel
pnpm install
```

运行

```bash
pnpm serve
```

大功告成。

## Copyright

```plaintext
/*
 * Copyright (c) 2022, Terwer . All rights reserved.
 * DO NOT ALTER OR REMOVE COPYRIGHT NOTICES OR THIS FILE HEADER.
 *
 * This code is free software; you can redistribute it and/or modify it
 * under the terms of the GNU General Public License version 2 only, as
 * published by the Free Software Foundation.  Terwer designates this
 * particular file as subject to the "Classpath" exception as provided
 * by Terwer in the LICENSE file that accompanied this code.
 *
 * This code is distributed in the hope that it will be useful, but WITHOUT
 * ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
 * FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License
 * version 2 for more details (a copy is included in the LICENSE file that
 * accompanied this code).
 *
 * You should have received a copy of the GNU General Public License version
 * 2 along with this work; if not, write to the Free Software Foundation,
 * Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA.
 *
 * Please contact Terwer, Shenzhen, Guangdong, China, youweics@163.com
 * or visit www.terwer.space if you need additional information or have any
 * questions.
 */
```
