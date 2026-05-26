---
layout:     post
title:      "GitHub Pages + Jekyll 搭建个人免费博客，超详细教程"
subtitle:   "零成本拥有自己的独立博客，5分钟搞定！"
date:       2026-05-25
author:     "JACK ZHANG"
header-img: "img/home-bg.jpg"
catalog: true
tags:
    - GitHub
    - 博客搭建
    - Jekyll
---

做技术分享、写学习笔记、建立个人品牌……你需要一个自己的博客。以前觉得建站很复杂，其实用 GitHub Pages + Jekyll，**完全免费，5分钟就能搞定**。

## 为什么选 GitHub Pages？

- 完全免费，无需购买服务器
- 支持自定义域名
- 自动部署，push 即发布
- Jekyll 主题丰富，颜值高

## 开始搭建

### 第一步：创建仓库

仓库名必须为 `{你的用户名}.github.io`，可见性选择 **Public**。

### 第二步：克隆模板

我用的是 Hux Blog 模板，直接克隆：

```bash
git clone https://github.com/huxpro/huxpro.github.io.git myblog
```

### 第三步：修改配置

编辑 `_config.yml`，改好标题、描述、博客地址等信息。

### 第四步：启用 GitHub Pages

进入仓库 → Settings → Pages，Source 选择 `main` 分支的 `/ (root)`，保存即可。

## 写文章

在 `_posts/` 目录下新建 `.md` 文件，命名格式：

```
YYYY-MM-DD-文章标题.md
```

文件开头加上 Front Matter 就能发布了。

> 博客地址：[https://love024star.github.io](https://love024star.github.io)

快去试试吧！
