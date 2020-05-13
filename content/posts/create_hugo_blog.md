---
title: "create_hugo_blog"
date: 2020-05-13T22:45:46+08:00
tags: ["搭建博客"]
categories: ["技术总结"]
---
# 搭建hugo静态博客记录

## 1 安装Hugo

  我这里是imac所以就直接用brew 其它操作系统也很简单 百度一下一把
```
brew install hugo
```

## 2 初始化站点目录 

  先cd到你想放置的磁盘目录 然后执行一下命令即可 会在当前目录创建站点名称同名目录

```
$ hugo new site blog                                       
Congratulations! Your new Hugo site is created in /Users/ketonghe/blog.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/ or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation.
```

## 3 安装主题并修改

  现在hugo主题商店挺多，我选择了相对干净的hugo-theme-pure  如果没有git环境 可自行百度安装

```
$ git clone https://github.com/xiaoheiAh/hugo-theme-pure themes/pure
Cloning into 'themes/pure'...
remote: Enumerating objects: 13, done.
remote: Counting objects: 100% (13/13), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 2527 (delta 2), reused 6 (delta 2), pack-reused 2514
Receiving objects: 100% (2527/2527), 4.14 MiB | 519.00 KiB/s, done.
Resolving deltas: 100% (1376/1376), done.
```

config.yml 配置文件主要修改项

```
baseURL 主页
menu  可以将下面的title改为对应的中文
donate 改为自己的微信和支付宝
profile 修改自己头像和介绍
```



## 4 写markdown文章

```
$ hugo new posts/helloworld.md            
/Users/ketonghe/blog/content/posts/helloworld.md created
```

用markdown编辑器编辑文章

## 5 发布预览

```
$ hugo server -D

                   | ZH  
+------------------+----+
  Pages            | 13  
  Paginator pages  |  0  
  Non-page files   |  0  
  Static files     |  9  
  Processed images |  0  
  Aliases          |  6  
  Sitemaps         |  1  
  Cleaned          |  0  

Total in 91 ms
Watching for changes in /Users/ketonghe/blog/{archetypes,content,data,layouts,static,themes}
Watching for config changes in /Users/ketonghe/blog/config.yml
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop

```

接下来就可以在本地浏览器 输入http://localhost:1313/  访问了

这个主题支持站内搜索 还不错 

## 6 添加评论支持

  参考 https://www.smslit.top/2018/07/08/hugo-valine/ 一步步来吧

## 7 生成静态页面

