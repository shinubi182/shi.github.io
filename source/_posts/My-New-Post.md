---
title: My New Post
date: 2022-05-27 14:26:18
tags:
---

##### 经过三天的折腾终于将博客部署倒github上

###### 第一部分: 环境准备

安装git,提前安装好

安装node.js，下载地址：https://nodejs.org/cn

Windows 电脑我是直接以管理员身份打开 cmd，输入:
查看 node 的版本：node -v
查看 npm 包管理器的版本：npm -v
因为 Hexo 需要 Nodejs 支持的、生成的，所以这是前置步骤。

###### 第二部分:安装 Hexo 博客框架

需借助 npm 包管理器来安装。因为国内安装镜像源很慢，所以利用 npm 安装 cnpm
用淘宝链接进行安装：`npm install -g cnpm --registry=https://registry.npm.taobao.org`

安装 Hexo 框架：`cnpm install -g hexo-cli`    `hexo -v`验证

直接在 E 盘自己手工创建了一个 blog 文件夹。所有博客的东西全部都在 blog 里面生成。所以大家如果出了什么错，直接连 blog 文件夹整个删除就行了。注意：千万不能只删除 blog 文件夹里面的内容，却不删除 blog 文件夹，这样操作会出问题的。

进入 blog 的目录中，位于这个目录下，就可以使用 Hexo 生成我们的博客。

初始化一个博客：`hexo init`

您看，它会自己去克隆。还会默认克隆一个 Landscape 主题:

###### 第三部分

看该目录下的所有子目录和文件：`ls -l`
启动博客：`hexo s`
输入[localhost:4000]()问下，看看博客是不是已经成功，已经有了

######  第四部分部署到GitHub

1.登录自己的 Github。
2.新建一个仓库：
注意：一定是你的昵称.github.io
例如我的 Github 昵称是 shinubi182，那么这里输入shinubi182.github.io

装 Git 部署的插件：`cnpm install --save hexo-deployer-git`

去 blog 文件下，直接看到一个_config.yml，修改_config.yml即可。注意：blog文件夹下的其它文件下也有_config.yml文件，别改错了文件。

文件的最底部修改成这样：
deploy:

```
  type: git
  repository: https://github.com/shinubi182/shinubi182.github.io.git
  branch: main
```

注意：deploy: type: repository: branch: 后面都有一个英文的空格。

用 nopad++修改后一定要保存！

部署到远端：`hexo d`

登录[shinubi182.github.io]()可以看到自己的博客了