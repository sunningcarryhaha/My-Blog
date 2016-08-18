---
title: Mysql-sql语法(入门)
date: 2016-07-21 13:57:37
tags: 
    - sql
    - mysql
    - 后台
author: CarryGuan
subtitle: 这是一个开始
---
![young](http://ww2.sinaimg.cn/large/005vGbJ7jw1f671ikpgnhj30s20as0v3.jpg)
* mysql-sql 语句  
* 字符集选utf-8
* 我需要学增删改查, 事物, 联合
***
## 启动数据库
<pre><code>
mysql -u root -p（root是用户名）
</code></pre>

## 查看数据库（所有）
<pre><code>
show databases
</code></pre>
<!--more-->

## 进入数据库
<pre><code>
use one ;
</code></pre>

##  展示当前数据库的所有表
<pre><code>
show tables;
</code></pre>

## 创建个名为user的表的结构
<pre><code>
create table user(
id int,
name  varchar(30),
pass varchar(30)
);（字符串长度最长是30）
</code></pre>

## 查看表结构
<pre><code>
desc user; 
</code></pre>

## 查看数据从表里面
<pre><code>
select * from user;
</code></pre>

## insert 增（我可以随意增加，插入数据到表中）
<pre><code>
 insert into table(ct1,ct2,ct3) values(num,"str","str")
 insert into user(id,name,pass) values(1,"leiwei","123")
</code></pre>

## 形成了下表

```
mysql> select * from user;
+------+-----------+------+
| id   | name      | pass |
+------+-----------+------+
|    1 | leiwei    | 123  |
|    2 | yujie     | 13   |
|    3 | qiancheng | 456  |
+------+-----------+------+
3 rows in set (0.00 sec)
```

## select 查（我可以随意查找 select from table where...）
<pre><code>
select * from user where id=2;
select * from user where pass=13;
</code></pre>

## select like 子段（ 我可以随意选取子字段 ）

```
select * from user where name like '%carry%';//选取中间含有carry字段的数据
+------+----------+------+
| id   | name     | pass |
+------+----------+------+
|    5 | carryone | 123  |
|    2 | carry    | 571  |
+------+----------+------+
```

### 选取以one结束的字段

```
select * from user where name like '%one';//
+------+----------+------+
| id   | name     | pass |
+------+----------+------+
|    5 | carryone | 123  |
+------+----------+------+
```

## select order by（排序我们可以随意排序数据） 
<pre><code>
        select * from user order by name; //默认是升序  
         select * from user order by id desc;//desc为降序排列
</code></pre>

## delete 删 （我可以随意删除 delete from table where...）

<pre><code>
delete from user where name="yujie";
delete from user where id=3;
</code></pre>

## update (我可以随意更改 update user set charct where ....)
<pre><code>
update user set name="billin" where id=1;
update user set id=5 where name="billin";
</code></pre>
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=5179544&auto=1&height=66"></iframe>
