---
layout: "post"
title: "好记性不如烂笔头"
date: "2018-12-15 19:03"
---

##### Windows启、停MySql
```
win+R 键入：

net start mysql
net stop mysql

注：windows不能直接restart Mysql;    如果是mysql 8.0，需要在命令后写mysql80
```
---

##### XML转义符 <br>
``` <br>
<    &lt;
>    &gt;
&    &amp;
”    &quot;
©    &apos;

注："&"和";"是成对的
```
---

##### list迭代异常`java.util.ConcurrentModificationException`
```
list迭代时会执行checkForComodification()，如果同时在进行add、remove、clear操作，就会抛出java.util.ConcurrentModificationException异常

解决：
方案a>单线程下使用迭代器Iterator时可以做remove
方案b>多线程加锁可达到方案a效果，如果需要进行其他操作，可以用CopyOnWriteArrayList

CopyOnWriteArrayList是读写分离的，实时性不足

注：Itr的remove方法有expectedModCount = modCount操作，ArrayList的remove方法没有
```
---

##### Mysql常用命令
```
mysql -u root -p --本地登陆
mysql -h host -u root -p  --远程登陆

create database new_dbname;--新建数据库
drop database old_dbnane; --删除数据库
show databases;--显示数据库
use databasename;--使用数据库
select database();--查看已选择的数据库

show tables;--显示当前库的所有表
create table tablename(fieldname1 fieldtype1,fieldname2 fieldtype2,..)[ENGINE=engine_name];--创建表
drop table tablename; --删除表
create table tablename select statement;--通过子查询创建表
desc tablename;--查看表结构
show create table tablename;--查看建表语句

alter table tablename add new_fielname new_fieldtype;--新增列
alter table tablename add new_fielname new_fieldtype after 列名1;--在列名1后新增列
alter table tablename modify fieldname new_fieldtype;--修改列
alter table tablename drop fieldname;--删除列
alter table tablename_old rename tablename_new;--表重命名

insert into tablename(fieldname1,fieldname2,fieldnamen) valuse(value1,value2,valuen);--增
delete from tablename [where fieldname=value];--删
update tablename set fieldname1=new_value where filename2=value;--改
select * from tablename [where filename=value];--查

truncate table tablename;--清空表中所有数据，DDL语句

show engines;--查看mysql现在已提供的存储引擎:
show variables like '%storage_engine%';--查看mysql当前默认的存储引擎
show create table tablename;--查看某张表用的存储引擎（结果的"ENGINE="部分）
alter table tablename ENGINE=InnoDB--修改引擎
create table tablename(fieldname1 fieldtype1,fieldname2 fieldtype2,..) ENGINE=engine_name;--创建表时设置存储引擎
```
---
