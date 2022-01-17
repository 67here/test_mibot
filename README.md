## [图床] 打造github和gitee的图床

### 一、用途
用来给自己的帖子、博客上传图片等资料，比如在支持MarkDown编辑器的论坛网站中，直接贴上链接，就可以直接展示出图片，不会受论坛自身的附件限制，国内的其它图床，或者是收费，或者是有效期限制，如果只是发发贴这种小需求，就可以借助免费的GitHub和gitee来做自己的图床，十分简便，这篇帖子就是如此。

### 二、开始制作
打造图床，只要在网页上配置即可，Picgo等软件只是额外的管理工具，非必要。

#### 1)方式1：改网址 

只需要新建库，上传图片，复制链接，三步，非常简单
效果如下
![](https://github.com/67here/test_mibot/blob/main/raw.png)
![](https://gitee.com/here67/picture_example/raw/master/tuchuang/raw.png)

这两张图片的代码是：

`![](https://github.com/67here/test_mibot/blob/main/raw.png)`

`![](https://gitee.com/here67/picture_example/raw/master/tuchuang/raw.png)`

github的也可以写成这样
`![](https://raw.githubusercontent.com/67here/test_mibot/main/raw.png)`

格式就是 https://github.com/用户名/库名/blob/分支名/文件名
这里master和main都是主分支的意思，gitee的格式也是如此，只不过中间需要多加一个raw
上面我贴出了两张图片，但是你很大概率只会看到一个gitee的图片，科学上网后就能看到两张，国内访问GitHub是不稳定的，解决方式是使用国内的CDN节点，下面会说，我自己在用的就是gitee，然后修改网址，效果比GitHub的CDN好的多。(缺点是 gitee限制图片大小1MB内)

#### 2）方式2：网页托管
它的用途是在没有个人域名和服务器的情况下依旧显示出完整的自定义网页，做图床有些大材小用，但也是个方法。

![](https://gitee.com/here67/picture_example/raw/master/tuchuang/01.jpg)

设置成功之后，项目的右下角会出现一个小火箭

![](https://gitee.com/here67/picture_example/raw/master/tuchuang/02.jpg)

代码示例：
`![](https://67here.github.io/picture_example/wuai_1/solve2.png)`

设置托管时，分支早已指定，所以网址里不再写。
相比于上面的方法，弊端是更新会略慢一点，不过GitHub在使用托管方式后，国内就基本上可以直接看了，不会出现上面图片不显示的情况，再配上CDN分流，效果会更好。

![](https://gitee.com/here67/picture_example/raw/master/tuchuang/03.jpg)

代码示例

`![](https://cdn.jsdelivr.net/gh/67here/picture_example@CDN/bear1.jpg)`

这里 **cdn.jsdelivr.net/gh** 是必须要加的前缀，CDN 是分支的名字

至于gitee的托管页面，它需要上传手持身份证，我不想上传，暂时没这个需求，所以我也不清楚里面的细节，算是偷了个懒，哈哈
![](https://gitee.com/here67/picture_example/raw/master/tuchuang/04.png)

