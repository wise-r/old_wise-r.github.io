---
layout: post
title:  "怎么使用WISER网站"
date:   2015-10-08 7:35:59
categories: 
- Policy 
tags:
- WISER

---





## Prequalification
---

> <http://wise-r.github.io/>是 WISER CLUB的官方主页。


1. [Github](https://github.com/) 账户
2. 加入[WISE-R](https://github.com/wise-r) organization， 并获得权限。
3. 安装[jekyll](http://jekyll.bootcss.com/)

### 申请Github账户

略

### 加入WISE－R

大家可以自行加入， 我会为大家配置权限

### 安装[jekyll](http://jekyll.bootcss.com/)

1. [Windows](http://www.madhur.co.in/blog/2011/09/01/runningjekyllwindows.html)
2. [Mac](http://jekyll.bootcss.com/docs/installation/) 貌似Mac是自带Ruby的

## Clone[WISER](https://github.com/wise-r/wise-r.github.io)
---


### 如果你没安装GIT
安装`Git`, 简单教程[廖雪峰教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)，目前你还不需要全部掌握

### Clone[WISER](https://github.com/wise-r/wise-r.github.io)

```
git clone git@github.com:wise-r/wise-r.github.io.git
```

## 更新blog
---

### 撰写blog

```
cd wise-r.github.io;
```

在`_posts`新建md文件，内容格式如里面的其它文件就是了。
文档命名`2010-10-08-xxxxx.md`

### 上传blog

```
git add .;
git commit -m "xxx";
git push -u origin master
```

稍等片刻，打开<http://wise-r.github.io/>就能看到你的blog了。

> 时间有些紧张，就简单的写一些，有疑问，请`Google`,或查看我用的模版<https://github.com/dbtek/dbyll>


