---
title: "使用hugo搭建博客"
date: 2019-12-26T12:15:46+08:00
draft: false
---

1. # 安装Hugo 
mac:
安装 Homebrew 直接在终端运行
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
然后直接使用 brew install hugo 即可

Windows:
在https://github.com/gohugoio/hugo/releases中的Assets下载windows压缩包,解压后配置系统path,即可在cmd运行hugo命令

2. # 配置hugo

1. 打开hugo官网 https://gohugo.io/
2.  点击 quick start
3.  执行step1-step7,7条命令
Step 1: Install Hugo
Step 2: Create a New Site
Step 3: Add a Theme
Step 4: Add Some Content
Step 5: Start the Hugo server
Step 6: Customize the Theme
Site Configuration
Step 7: Build static pages

3. # 安装主题,生成网站

一般的主题都会托管在 Github，可以直接下载,`git clone --depth 1 --recursive https://github.com/gohugoio/hugoThemes.git` themes
如果本地没有安装 Git，那么你也可以直接下载该主题的 zip 打包文件，并解压到 themes 目录，然后修改 config.toml,运行 `hugo server -D `即可访问 `http://localhost:1313`

1. # 发布blog
运行`hugo new 文章.md`,会生成到content文件夹

2. # 托管github pages

在 GitHub 上创建一个 Repository，命名为 githubusername.github.io
把config.toml里的 basaeURL 修改为 https://githubusername.github.io
运行`hugo`,生成public目录,然后进入你的 public 目录按照正常 Git 命令操作即可

* 注意:public存放html文件,与生成器代码需要放在两个仓库托管