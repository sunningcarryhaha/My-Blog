---
title: MyVocation
date: 2016-08-16 09:09:04
tags:
     - vocation
     - life
     - work
     - vocation summing
     - 暑假生活
author: CarryGuan
subtitle: 我的暑假
---
# 一共四周：
第一周：了解一下做的是啥，学习mysql,node.js,coffeescript,socket
第二周 : 写了缺货提醒的接口(warehouse-coffee-lib--timer-newStocksInfor),获得缺货详细列表的接口(warehouse-coffee-lib-getStocksList)
第三周：写了获得缺货门店的信息接口(warehouse-coffee-lib-AreaLacks)
第四周：学express,node.js搭建网站，写后台
<!--more-->
# 后台工作流程：
## 一：搭建服务器
## 二：数据处理：
数据库（mysql）,redis,memcache
## 三：本机启动后台系统 
node main.js/supervisor main.js/NODE_ENV=DEV &&supervisor main.j
## 四：与客户端的连接
### 1:
此客户端可以为android,ios,web前台（前端）
### 2:
客户端需要知道后台的ip,进行 ping连接
### 3:
客户端也需要知道与后台进行交互的那个接口
## 五：和客户端的交互

后台需要写好接口功能，并把数据通过这个接口传输给客户端(socket.on)
后台自己定义好功能（一般是客户端的系统信息推送）自发起一个接口(socket.emit),客户端soket.on接口和数据

## 六：注意
从github拽下来的文件，需要进入其跟目录进行npm install,原因是将package.json中的dependencies依赖包进行下载；
# More
真的特别感谢公司给的这次机会，让我学到了好多新知识，还结交到了几位盆友，跟他们这样有多年开发经验的人沟通，了解了开发方式与模式，扩展了知识面
***
# 最后
[图片爸爸加载](http://www.jianshu.com/p/25e89c1ad4ab)
放一张我男神BI照片来开心一下（原谅博主少女心）
![](http://upload-images.jianshu.io/upload_images/2377897-895ca3735e03828e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
再放一张博主我的（表杀我，咩咩）
![](http://upload-images.jianshu.io/upload_images/2377897-1e9289634631a1cc.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
