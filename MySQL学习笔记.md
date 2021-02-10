# MySQL学习笔记

[TOC]



## MySQL预留字集合

| ADD                | ALL                 | ALTER              |
| ------------------ | ------------------- | ------------------ |
| ANALYZE            | AND                 | AS                 |
| ASC                | ASENSITIVE          | BEFORE             |
| BETWEEN            | BIGINT              | BINARY             |
| BLOB               | BOTH                | BY                 |
| CALL               | CASCADE             | CASE               |
| CHANGE             | CHAR                | CHARACTER          |
| CHECK              | COLLATE             | COLUMN             |
| CONDITION          | CONNECTION          | CONSTRAINT         |
| CONTINUE           | CONVERT             | CREATE             |
| CROSS              | CURRENT_DATE        | CURRENT_TIME       |
| CURRENT_TIMESTAMP  | CURRENT_USER        | CURSOR             |
| DATABASE           | DATABASES           | DAY_HOUR           |
| DAY_MICROSECOND    | DAY_MINUTE          | DAY_SECOND         |
| DEC                | DECIMAL             | DECLARE            |
| DEFAULT            | DELAYED             | DELETE             |
| DESC               | DESCRIBE            | DETERMINISTIC      |
| DISTINCT           | DISTINCTROW         | DIV                |
| DOUBLE             | DROP                | DUAL               |
| EACH               | ELSE                | ELSEIF             |
| ENCLOSED           | ESCAPED             | EXISTS             |
| EXIT               | EXPLAIN             | FALSE              |
| FETCH              | FLOAT               | FLOAT4             |
| FLOAT8             | FOR                 | FORCE              |
| FOREIGN            | FROM                | FULLTEXT           |
| GOTO               | GRANT               | GROUP              |
| HAVING             | HIGH_PRIORITY       | HOUR_MICROSECOND   |
| HOUR_MINUTE        | HOUR_SECOND         | IF                 |
| IGNORE             | IN                  | INDEX              |
| INFILE             | INNER               | INOUT              |
| INSENSITIVE        | INSERT              | INT                |
| INT1               | INT2                | INT3               |
| INT4               | INT8                | INTEGER            |
| INTERVAL           | INTO                | IS                 |
| ITERATE            | JOIN                | KEY                |
| KEYS               | KILL                | LABEL              |
| LEADING            | LEAVE               | LEFT               |
| LIKE               | LIMIT               | LINEAR             |
| LINES              | LOAD                | LOCALTIME          |
| LOCALTIMESTAMP     | LOCK                | LONG               |
| LONGBLOB           | LONGTEXT            | LOOP               |
| LOW_PRIORITY       | MATCH               | MEDIUMBLOB         |
| MEDIUMINT          | MEDIUMTEXT          | MIDDLEINT          |
| MINUTE_MICROSECOND | MINUTE_SECOND       | MOD                |
| MODIFIES           | NATURAL             | NOT                |
| NO_WRITE_TO_BINLOG | NULL                | NUMERIC            |
| ON                 | OPTIMIZE            | OPTION             |
| OPTIONALLY         | OR                  | ORDER              |
| OUT                | OUTER               | OUTFILE            |
| PRECISION          | PRIMARY             | PROCEDURE          |
| PURGE              | RAID0               | RANGE              |
| READ               | READS               | REAL               |
| REFERENCES         | REGEXP              | RELEASE            |
| RENAME             | REPEAT              | REPLACE            |
| REQUIRE            | RESTRICT            | RETURN             |
| REVOKE             | RIGHT               | RLIKE              |
| SCHEMA             | SCHEMAS             | SECOND_MICROSECOND |
| SELECT             | SENSITIVE           | SEPARATOR          |
| SET                | SHOW                | SMALLINT           |
| SPATIAL            | SPECIFIC            | SQL                |
| SQLEXCEPTION       | SQLSTATE            | SQLWARNING         |
| SQL_BIG_RESULT     | SQL_CALC_FOUND_ROWS | SQL_SMALL_RESULT   |
| SSL                | STARTING            | STRAIGHT_JOIN      |
| TABLE              | TERMINATED          | THEN               |
| TINYBLOB           | TINYINT             | TINYTEXT           |
| TO                 | TRAILING            | TRIGGER            |
| TRUE               | UNDO                | UNION              |
| UNIQUE             | UNLOCK              | UNSIGNED           |
| UPDATE             | USAGE               | USE                |
| USING              | UTC_DATE            | UTC_TIME           |
| UTC_TIMESTAMP      | VALUES              | VARBINARY          |
| VARCHAR            | VARCHARACTER        | VARYING            |
| WHEN               | WHERE               | WHILE              |
| WITH               | WRITE               | X509               |
| XOR                | YEAR_MONTH          | ZEROFILL           |

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

### 先启动再登录

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

## 基本的查询语句

### 1.查询所有的数据

```mysql
select * from person;
```

### 2.查询部分信息

```mysql
select name,phone from person;
-- 指定列名进行查询

-- 特别注意，当存在多个数据库时要使用数据库名.表名的形式书写表，例如：
select name, age from demo.person;

-- 指定列名
select name as '名字' ,phone as '电话' from person;
```

### 3.最基本语法

```mysql
select *(全部)/列1,列2... from 表;
```

### 4.带条件的查询

```mysql
-- where查询

select * from 表 where 查询条件 = 'xxxx';

select * from person where name = 'zhuyuanzhang';

-- 大于、小于、等于、范围的判断
select * from person where age > 20; -- 挑选大于二十岁的人
select * from person where age <= 20; -- 挑选小于等于二十岁的人
select * from person where age between 18 and 20; -- 挑选年龄介于十八岁到二十岁之间的人
-- 相当于 age >= 18 && age <= 20;

-- 不等于
select * from 表 where 列名 != 'xxx';

-- 判空操作
select * from 表 where 列名 is null;
select * from 表 where 列名 is not null;

-- 模糊搜索
select * from 表 where 列名 like 'xxx';

-- 查询包含在某数据集中的数据
select * from 表 where 列名 in (数据集);
```

### 5.模糊搜索

```mysql
-- 模糊搜索
select * from 表 where 列名 like 'xxx';
-- 注意搜索条件关键词后通常跟着占位符，其中%代表任意数量和内容的字符，_(下划线)仅代表一个字符，例如：
select * from person where name like 'zhu%'; -- 只要名字开头带zhu的都会被列出
select * from person where name like 'zhu__'; -- 名字开头有zhu且zhu后面仅有两个字符的才会被选出
select * from person where name like '%zhan%'; -- 只要名字里带zhan的都会被列出
```

### 6.查询包含在某数据集中的数据

```mysql
-- 查询包含在某数据集中的数据
select * from 表 where 列名 in (数据集);

select * from demo.person where age in (24, 25);
```

