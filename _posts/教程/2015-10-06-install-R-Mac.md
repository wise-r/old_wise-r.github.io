---
layout: post
title:  "Mac下安装R和Rstudio"
date:   2015-10-06 11:35:59
categories: 
- 教程
tags:
- R
- RStudio
- Mac

---

<section id="table-of-contents" class="toc">
  <header>
    <h3>Overview</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->


> 本教程参考：[Window下安装R和Rstudio](http://changshun.github.io/tutorial/2015/10/06/Window%E4%B8%8B%E5%AE%89%E8%A3%85R%E5%92%8CRstudio.html)

## 1.安装R 

### 1.1 下载R
---

你能够从<http://mirrors.xmu.edu.cn/CRAN/>上下载最新的`R`. 
![Path](http://i.imgbox.com/CG0TTtSs.png)


### 1.2 安装R
---


![](http://i.imgbox.com/Z7H0za0A.png)

**注意**: 尽量不要安装到中文路径下， 以后使用时可能会有麻烦


![bit](http://i.imgbox.com/xS53DAon.png)

![成功](http://i.imgbox.com/Z7H0za0A.png)

## 2. 安装RStudio
---

### 2.1 下载RStudio
---

你能够从[RStudio官网](https://www.rstudio.com/)上下载最新的`RStudio`. 
![Path](http://i.imgbox.com/tK6TOXLp.png)

### 2.2 安装RStudio
---
![](http://i.imgbox.com/CrbrYKfx.jpg)

![](http://i.imgbox.com/2yJKBFtP.png)


## 3. 更新R
---
### 3.1 Fool Way

1. 备份你的程序包
重新安装R软件时可能会把你已经安装的`package`覆盖， 为了避免，我们需要先进行备份(将`library`文件夹复制到他处)。
  
程序包位置：`/Library/Frameworks/R.framework/Versions/3.2/Resources/library`

**如何进入路径**
> 打开`finder`, 使用`⌘(command)+⇧（shift）+G`, 输入上面路径就可以进入路径
![path2](http://i.imgbox.com/K68vFhUO.png)

2. 重复`1.1`和`1.2`



### 3.2 The Harder Way
---

Now we set up the global library for R. More details about this is described in [Tal Galili's blog post][1]. Although you are using the latest version of R, you can still follow my steps. It will help you set a global library for R. This will prevent some troubles in the future.

Open your R. Run `chooseCRANmirror()` command line(Type it and hit `ENTER`) .Choose `China(Xiamen)`.

![mirror](http://i.imgbox.com/nMC12nzx.jpg "Choose Mirror")

Run the following codes line by line.
```
source("http://www.r-statistics.com/wp-content/uploads/2010/04/upgrading-R-on-windows.r.txt")
Old.R.RunMe()
```

![oldr](http://i.imgbox.com/yn5SmnIH.jpg "Set global lib")

It will ask you whether or not to quit R. Just type `n` and hit `ENTER`. Then run `New.R.RunMe()` just the same way.


Once you have done these, from now on, whenever you want to update to a new version of R in the future, all you will need to do are the following **TWO** steps:

1. Download and install the new version of R
2. Open your new R and run the following codes

{% highlight R %}
source("http://www.r-statistics.com/wp-content/uploads/2010/04/upgrading-R-on-windows.r.txt")
New.R.RunMe()
{% endhighlight %}



