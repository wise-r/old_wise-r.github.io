---
layout: post
title:  "Window下安装R和Rstudio"
date:   2015-10-06 10:35:59
categories: 
- 教程
tags:
- R
- RStudio
- Windows
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

<div class="mod_player" id="mod_player"><div id="mod_tenvideo_flash_player_1444705896923"><embed wmode="window" flashvars="vid=e0168csx1k6&amp;tpid=3&amp;showend=1&amp;showcfg=1&amp;searchbar=1&amp;shownext=1&amp;list=2&amp;autoplay=1&amp;ptag=www_baidu_com&amp;outhost=http%3A%2F%2Fv.qq.com%2Fpage%2Fe%2Fk%2F6%2Fe0168csx1k6.html&amp;openbc=0&amp;title=%20Windows%E7%8E%AF%E5%A2%83%E4%B8%8B%E5%AE%89%E8%A3%85R%E5%92%8CR%EF%BC%8Dstudio" src="http://imgcache.qq.com/tencentvideo_v1/player/TencentPlayer.swf?max_age=86400&amp;v=20140714" quality="high" name="tenvideo_flash_player_1444705896923" id="tenvideo_flash_player_1444705896923" bgcolor="#000000" width="650px" height="472px" align="middle" allowscriptaccess="always" allowfullscreen="true" type="application/x-shockwave-flash" pluginspage="http://get.adobe.com/cn/flashplayer/"></div></div>

## 1.安装R 

### 1.1 下载R
---

你能够从<http://mirrors.xmu.edu.cn/CRAN/>上下载最新的`R`. 
![Path](http://i.imgbox.com/VGVYmBnr.png)


### 1.2 安装R
---
![CRAN](http://i.imgbox.com/8GDBWR9w.png)

**注意**: 尽量不要安装到中文路径下， 以后使用时可能会有麻烦


![bit](http://i.imgbox.com/sHKrGASq.png)

![成功](http://i.imgbox.com/nQ7cCpWC.png)

## 2. 安装RStudio
---

### 2.1 下载RStudio
---

你能够从[RStudio官网](https://www.rstudio.com/)上下载最新的`RStudio`. 
![Path](http://i.imgbox.com/tK6TOXLp.png)

### 2.2 安装RStudio
---
![](http://i.imgbox.com/fzKEm7t5.png)

![](http://i.imgbox.com/iCe2KoYK.png)


## 3. 更新R
---
### 3.1 Fool Way

1. 备份你的程序包
重新安装R软件时可能会把你已经安装的`package`覆盖， 为了避免，我们需要先进行备份(将`library`文件夹复制到他处)。  
程序包位置：`C:\XXX\R\R-3.2.2\library`
![path2](http://i.imgbox.com/oRnNGM5x.png)

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



