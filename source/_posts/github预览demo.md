---
title: Github预览demo
date: 2016-07-15 13:18:04
tags: 
    - demo 
    - githubPages 
author: CarryGuan
subtitle: 我要看网页的效果
---
![young](http://upload-images.jianshu.io/upload_images/2377897-fc915701514c515c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 问题所在？
* 解决办法？
* 博主建议？
(原谅博主carry比较变态，在博文加了歌曲，不想听歌的小胖友们可以到博文底部关闭 ^~^)
图片无法加载可以点击[图片爸爸](http://www.jianshu.com/p/75e30889e70a)
***
## 一：问题的所在
相信很多小胖友们在把自己的网页上传到github仓库中，都会有一个疑问？是什么呢？
那就是上传完网页后，自己的仓库中是这个样子的![](http://upload-images.jianshu.io/upload_images/2377897-44104fdfe222e566.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)，点进去相应的html文件是出来的是代码![](http://upload-images.jianshu.io/upload_images/2377897-933438f6e1551351.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
可是自己想在网上看到自己仓库中的demo(也就是网页的效果)
下面博猪为您解答 (^~^)
***
<!--more-->
## 二：解决问题的方法
####  1: 使用 Githubpages
   比如我要上传![](http://upload-images.jianshu.io/upload_images/2377897-5b4113b7f687b1e5.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
   按照如下四个步骤上传到名为:flexSupplement的仓库中
```
     git init (初始化本地仓库)
     git add .  （将本地所有文件加到仓库里）
     git commit -m "message" （设置提交信息）
     git remote add origin   git@github.com:sunningcarryhaha/flexSupplement.git（本地仓库链接远程仓库）
     git push -u origin master （push文件到仓库中）

``` 
上传成功后是这个效果![]()
重头戏来了哟！
我们现在点击这个html文件，出现的效果全是代码![]![](http://upload-images.jianshu.io/upload_images/2377897-933438f6e1551351.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)()，没有咱们想要的demo效果
此时呢，应该植入咱们github爸爸的一个好东西，那就是-githubPages
##### 第一步：找到Settings
    ![](http://upload-images.jianshu.io/upload_images/2377897-0a301fa6cbc3d33f.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
##### 第二布：找到githubPages
![](http://upload-images.jianshu.io/upload_images/2377897-5033f61187c659c7.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
##### 第三步：预览githubPages
![](http://upload-images.jianshu.io/upload_images/2377897-794ba43a2fadab1d.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
小胖友们看到这里一定会有疑问，预览到的是githubpages的效果，并不是你自己网页的效果，没关系，我下面为你们解答
##### 第四步：查看你的分支
![](http://upload-images.jianshu.io/upload_images/2377897-2fdf9314d74b1a05.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
注意：我们生成githubPages的目的就是需要生成一个gh-pages分支(咱们正常情况下只有一个master分支)
##### 第五步：将远程仓库克隆到本地
<pre><code>
$ git clone git@github.com:sunningcarryhaha/flexSupplement.git
</code></pre>
##### 第六步：将分支切换到gh-Pages
<pre><code>
  $ cd flexSupplement （进入到你克隆仓库的本地文件夹）
  $ git checkout gh-pages（将master分支切换到gh-pages分支上）
 
</code></pre>
###### 第七步：并重新上传到github上
将本地克隆的文件删了，只留下.git,然后把你想要展示demo页面相关的文件粘进去
接着，执行以下语句
<pre><code>
 git add . （将本地所有文件加到仓库里） 
 git commit -m "message" （设置提交信息） 
 git remote add origin git@github.com:sunningcarryhaha/flexSupplement.git（本地仓库链接远程仓库） 
 git push -u origin gh-pages （push文件到仓库中）
</code></pre>
##### 第八步：修改地址
我的GithubPages地址是这个：http://carryguan.me/flex-add
我要预览flex-add中的fb1.html
我最后预览的地址应该是这个：http://carryguan.me/flex-add/fb1.html
##### 第九步：添加read.me
把地址放到read.me中
<pre><code>
  flex-add
  这是一个关于flexbox基础的骰子布局
  [demo](http://carryguan.me/flex-add/fb1.html)  
</code></pre>
#### 2: 增加路径前缀（不建议用，会自动更改css的样式）
在地址前加[http://htmlpreview.github.io/?](http://htmlpreview.github.io/?)前缀（不建议用这个，会更改css样式）
例如，你想预览这个：
</br>[https://github.com/aisinvon/aisinvon.github.io/blob/master/index.html]()
</br>
你在这个地址前加[http://htmlpreview.github.io/?](http://htmlpreview.github.io/?)
</br>
最后预览demo地址是：
http://htmlpreview.github.io/?https://github.com/aisinvon/aisinvon.github.io/blob/master/index.html
***
 博主感想

希望有更多小胖友提出宝贵意见,若有关于前端的问题，或者关于大学方面的感想可以私聊我(^~^)：

[github](https://github.com/sunningcarryhaha)
[知乎](https://www.zhihu.com/people/guan-kai-li-88)
[简书](http://www.jianshu.com/users/0293a04839f0/latest_articles)
[微博](http://weibo.com/u/5048785433/home?wvr=5)
***
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=28756834&auto=1&height=66"></iframe>
