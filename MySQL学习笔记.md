# MySQL学习笔记

## MySQL软件介绍

### MySQL产品特点

1.成本低，开源免费

2.性能高，执行很快

3.简单，易于使用

### DBMS分类

基于共享文件系统的DBMS

基于客户机——服务器的DBMS

### 软件卸载

控制面板卸载+清理残留文件

### 软件安装

按照安装步骤运行就行

经典、自定义和完全安装

要求：非中文没有空格

## MySQL服务的启动和停止

### 第一种方式

计算机--右击--管理--服务和应用程序--服务--MySQLxxx

根据需求设定启动方式

### 第二种方式

命令行窗口（管理员身份）

停止：net stop mysql***(MySQL服务名)

运行：net start mysql***(MySQL服务名)

## MySQL的登录和退出

### **先启动再登录**

第一种方式

MySQL自带客户端；退出exit/Ctrl+c（只用于root）

第二种方式吧

命令行

mysql -h（主机名） localhost -P(端口号) 3306 -u（用户名）-p（密码）

 

e.g.: mysql -h localhost -P 3306 -u root -p passwd

## 基本的DDL语句

 

### 数据库系统分类

1.DB 			数据库：存储数据

2.DBMS		管理数据的



### DBMS

1.DCL  数据控制语言：用于创建和维护用户账户的

2.DDL  数据定义语言：定义数据结构

3.DML  ：用来操纵数据的（难度系数小）



### DDL

#### 1.如何操纵数据库（创建和删除）

​	创建数据库：

```mysql
creare database 数据库名
```

​	删除数据库：

```mysql
drop database 数据库名
```

​	删除数据库时加入条件判断：

```mysql
drop database if EXISTS 数据库名
```

#### 2.注释写法

多行注释

```mysql
/* 


*/
```

单行注释

```mysql
-- 内容
```

3.创建表

```mysql
create table 表的名字(

		--字段（表头，column，列）

		字段名 类型（长度）约束,
    	其他字段。。。。。。

);
```

