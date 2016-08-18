---
layout:     
title: "最详尽-hexo+GithubPages搭建博客"  
date: 2016-07-02
author: "Carry Guan"
tags:
    - hexo
    - blog
---
![](http://ww1.sinaimg.cn/large/005vGbJ7jw1f5ms460e6tj30zk0aqgn1.jpg)
* 为什么选择hexo？
* 搭建博客的基本步骤
* 部署到Github Pages
* 域名解析
(原谅博主carry比较变态，在博文加了歌曲，不想听歌的小胖友们可以到博文底部关闭 )
图片无法加载可以点击[图片爸爸](http://www.jianshu.com/p/0321cb243963)
***
## 为什么选择hexo？
Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 [Markdown](http://daringfireball.net/projects/markdown/)（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。
***
## 搭建博客的基本步骤

* 购买域名
* 安装hexo
* 注册github

### 一：购买域名
   若小胖友们想把个人博客挂到属于自己的域名上，博主在这里建议大家提前把域名买好。
博主购买域名的地方是[万网](https://wanwang.aliyun.com/),注册登录后，填写你想要的域名
<!--more-->
![](http://upload-images.jianshu.io/upload_images/2377897-a9273887335cde2a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
选择完自己域名后，付费就可以了！
(博主建议个人域名选择.me为后缀的较好-博主的域名就为[carryguan.me](http://carryguan.me))


### 二：安装hexo
  装 Hexo 相当简单。然而在安装前，您必须检查电脑中是否已安装下列应用程序：
[Git](http://git-scm.com/)
[Node.js](http://nodejs.org/)

 若你是IT小白，安装git/node没成功,博主carry给你个福利贴士
 (博主就是这样一点点过来的 （＃￣▽￣＃）)
[windows安装git](http://jingyan.baidu.com/article/90895e0fb3495f64ed6b0b50.html)
[windows安装node.js](http://jingyan.baidu.com/article/b0b63dbfca599a4a483070a5.html)

>在这里建议小胖友们，先预习一下:   
  [git入门教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
[github趣味详解](https://www.zhihu.com/question/20070065)

如果您的电脑中已经安装上述必备程序，那么恭喜您！接下来只需要使用 npm 即可完成 Hexo 的安装。
先进入一个文件夹路径：例如我的![](http://ww3.sinaimg.cn/large/005vGbJ7jw1f5fbuje1hjj30l50bd75k.jpg)
再执行下面的命令:
<pre><code>npm install -g hexo-cli</code></pre> 

### 初始化框架
#### 1执行如下语句
<pre><code> hexo init blog</code></pre>

 (blog是我自己建立的用来装博客的文件夹)


#### 2：再执行

<pre><code>cd blog</code></pre> 



#### 3: 最后执行
<pre><code>npm install</code></pre> 

以上三条语句执行完毕后， 你会在blog文件夹里看到如下: 
 ```
 ├── _config.yml //网站的配置信息，您可以在此配置大部分的参数。 
 ├── package.json 
 ├── scaffolds //模版文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。 
 ├── source //资源文件夹是存放用户资源的地方。
  | ├── _drafts
  | └── _posts 
 └── themes //主题文件夹。Hexo会根据主题来生成静态页面。
```
 #### 最后看看你自己的个人网站：
在blog目录下执行gitbash命令:

1：新建一篇文章（我的第一篇文章）

<pre><code>
 hexo new "我的第一篇文章"
</code></pre> 

会在/source/_post里自动生成了“我的第一篇文章.md”文件，之后新建的文章都将存放在此目录下。编辑“我的第一篇文章.md”文件可修改内容。

2：生成网站

<pre><code> 
hexo generate (可简写成 hexo g)
</code></pre> 

3:启动本地服务器

<pre><code> 
 hexo server (可简写成 hexo s)
</code></pre> 


4:在浏览器输入[http://localhost:4000](http://localhost:4000/) 即可查看网站。
### 三：注册github

[github](https://github.com/)
填写完相应信息，注册成功后，重新登录，进入到这个页面
![](http://ww2.sinaimg.cn/large/005vGbJ7jw1f5md7zebr5j30wp0gnq5f.jpg)
点击图片中所圈位置出现了如下：
![](http://ww4.sinaimg.cn/large/005vGbJ7jw1f5mdn65brmj30ng0h0dh1.jpg)
>Repository name里填写:你的用户名.github.io
(例如我的用户名是[sunningcarryhaha](https://github.com/sunningcarryhaha),所以我的Repository name:sunningcarryhaha.github.io)
Description里随便填一下你的描述就好
Public选中
选中Initilize this respository with a README
最后点击绿色按钮创建

![](http://ww4.sinaimg.cn/large/005vGbJ7jw1f5mdofjeuij30pv0k9tab.jpg)
创建成功后
配置SSH-Key
[详细步骤请点击此文章](http://jingyan.baidu.com/article/a65957f4e91ccf24e77f9b11.html)

***

## 将blog部署到Github Pages 上

** 两种方法:**

* 使用hexo deploy部署
* 使用git push 部署
### 1：hexo deploy部署
#### 配置deploy
找到blog目录下的配置文件_config.yml,用编辑器打开此文件
找到此文件中的deploy字段，按照以下配置
      deploy: 
       type: git 
       repo: git@github.com:sunningcarryhaha/sunningcarryhaha.github.io.git   
       branch: master
#### 注意需要提前安装一个扩展：
       $ npm install hexo-deployer-git --save
#### 然后在命令行中执行
         hexo d
>不幸的是，上述命令虽然简单方便，但是偶尔会有莫名其妙的问题出现，因此，我们也可以追本溯源，使用git命令来完成部署的工作。

### 2:使用gitbash，将public文件夹上传到自己的仓库中

#### 第一步：进入到你的blog目录

<pre><code> 
 cd blog
</code></pre>
 
#### 第二步 :初始化博客

<pre><code>
hexo g
</code></pre> 

#### 第三步:把public文件夹上传到github仓库中

<pre><code> 
cd public
</code></pre> 

```
git init (初始化本地仓库)
git add .  （将本地文件加到仓库里）
git commit -m "message" （设置提交信息）
git remote add origin git@github.com:sunningcarryhaha/sunningcarryhaha.github.io.git（本地仓库链接远程仓库）
git push origin master （push文件到仓库中）

```

>    
git@github.com:sunningcarryhaha/sunningcarryhaha.github.io.git 
解释一下   ：
sunningcarryhaha是用户名
sunningcarryhaha.github.io是仓库名称
.git是后缀

详细的步骤可参考此
[github push](http://blog.csdn.net/steven6977/article/details/10567719)
[git github 问题总结](http://blog.csdn.net/chaihuasong/article/details/37911723)

部署成功以后，在浏览器中输入你的repository名字：例如我的[sunningcarryhaha.github.io](https://github.com/sunningcarryhaha)
#### 就可以看到你的网站了
***
## 域名解析
* 进入万网进行域名绑定
* 进入public,新建CNAME
* 把域名写到CNAME里
* 传到github仓库里
### 1:进入万网进行域名绑定
  ![](http://ww4.sinaimg.cn/large/005vGbJ7jw1f5feoitevaj30ah0bit9r.jpg)
![](http://ww1.sinaimg.cn/large/005vGbJ7jw1f5fepmf432j31hb0jgthk.jpg)
![](http://ww3.sinaimg.cn/large/005vGbJ7jw1f5fer7xepxj319r0d2gpx.jpg)
安照以上图片进行操作
 ** 尤其注意:记录值那里填写的是:sunningcarryhaha.github.io.，也就是你的仓库名字后还有个"."  **
以上进行完毕后，接着下一步
 
### 2:进入blog下的public文件夹,新建 CNAME

![](http://ww4.sinaimg.cn/large/005vGbJ7jw1f5fe1tnb1pj30rt0h5q7d.jpg)
![](http://ww4.sinaimg.cn/large/005vGbJ7jw1f5feuzv6ncj30ip0e5gn3.jpg)
### 3:将public文件夹下的CNAME上传到github仓库中
 ![](http://ww2.sinaimg.cn/large/005vGbJ7jw1f5feyzubl7j30l50bdq5p.jpg)
如果上传成功的话，进入到你的github仓库中会看到CNAME文件
![](http://ww3.sinaimg.cn/large/005vGbJ7jw1f5ff5aey6gj30sj0ndn3i.jpg)
### 4:为了防止域名解析出问题
博主建议将blog下的public下的CNAME文件，复制到blog下的source文件夹里，这样更新public，不会出现CNAME文件丢失的情况
***
如果以上步骤都进行完毕的话，博主carry恭喜你:bowtie:,小胖友你zen棒，现在在浏览器输入你的域名，就可以成功的看到你的个人网站啦！
当然这个网站还可以换主题，美化！这方面的文章敬请期待，博主会继续出博文的!
*** 
## 博主感想
这个博客博主搭建了好久，走了好多弯路(原谅博主比较笨，呜呜！)
期间出了好多问题，最根本的原因是博主git方面不基础不好,所以建议小胖友们多练习一下git
这里推荐:
     [git入门教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
    [node.js安装菜鸟教程](http://www.runoob.com/nodejs/nodejs-install-setup.html)
   [hexo官网](https://hexo.io/zh-cn/docs/index.html)
[markdown入门](http://www.jianshu.com/p/1e402922ee32/)
[hexo主题推荐](https://www.zhihu.com/question/24422335/answer/46357100)
[next-hexo主题](http://theme-next.iissnan.com/)
[hexo常见问题解决方案](http://wp.huangshiyang.com/hexo%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88)

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=3412579&auto=1&height=66"></iframe>
