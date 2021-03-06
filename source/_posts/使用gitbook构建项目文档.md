---
layout: post
title: gitbook构建项目文档
date: 2018-01-14
categories: 技术
---


## gitbook使用入门
### 基本使用

* 安装gitbook(需要先安装node获取npm)
>`npm install gitbook-cli -g`
* 创建book
>`gitbook init`
* 构建并运行book/构建编译gitbook
>`gitbook serve`/`gitbook build`

### 目录结构
```
|---book.json(book配置信息) 
|---README.md(book首页)
|---SUMMARY.md(book目录说明)
|---_book/(编译后静态文件)
|---node_modules(模块文件)
```

### 配置信息
(<code>用于管理book配置,主题,插件等信息<code>)
* title - 标题
* author - 作者
* root - book根目录
* structure - 结构说明,可指定`REAME.md`等文件
* description - book简介
* isbn - book国际编号
* language - 语言,默认`en`
* direction - 文字书写方向
* gitbok - gitbook版本
* plugins - 插件,主题信息
* pluginsConfig - 插件,主题配置信息

### 主题
*仅提供参考,如果想要了解更多,可以npm查询gitbook-theme*

* `-fontsettings` ---用于自定义文字颜色等

### 插件
*仅提供参考,如果想要了解更多,可以npm查询gitbook-plugins*

* `page-treeview` --- 生成当前页目录结构
* `anchor-navigation-ex` --- 管理当前也目录结构
* `simple-page-toc` --- 增加回到顶部功能

[gitbook使用官方文档]("https://toolchain.gitbook.com")










    
