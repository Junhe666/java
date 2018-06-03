##### 连接Mysql

一、打开数据库服务：控制面板-->管理工具-->服务-->启动MySQL服务
二、运行：cmd   --> mysql -u用户名(root)  -p密码



##### SQL：
 结构化查询语言，是关系型数据库进行通信的标准语言。TSQL
关系型数据库：由被称为表的逻辑单元组成，这些表在数据库内部彼此关联。

##### Sql命令的类型：

##### 主要的分类：
  数据定义语言（DDL）：创建数据库对象和重构数据库对象，比如创建表和删除表

  数据操作语言(DML): 增 删 改

  数据查询语言(DQL)：查 

  数据控制语言(DCL):通常用户创建和访问用户对象

  数据管理命令：

  事物控制命令：



##### 命令：

Sql语句以分号 ; 作为命令的结束符号。


show databases;  查询所有的数据库

use  数据库名称;  进入到某一个数据库的领域   例如：use mysql

show tables;  查询该数据库中的所有数据表
 
select * from 表名; 查询表

Describe 表名;  查看表结构

Exit; 退出数据库

创建数据库
命名规范：
      特别是表和列的名称，应该让名称反应出所保存的数据。

创建一个数据库：school
语法： create database 数据库名;

       例： create database school;
删除数据库：

语法：drop database 数据库名;

      例：drop database school;
   

创建表：
	
创建一张表的语法：

进入到数据库：

Use school; 进入到数据库school

Create table 表名; 

例如：
Create table studends(studendName varchar(10) );


修改表：  
alter table 表名;  当表被创建时可用该命令修改。

Alter table 原表名 rename to 新表名;

Alter table studends rename to studend;  // 修改表名

删除表：

 drop table 表名;

 drop table studend;

修改列名：

Alter table 表名 change 原列名 新列名 新列数据类型;
Alter table studend change studendName studentName varchar(10);

增加列：

Alter table 表名add 要增加的列名 数据类型;

Alter table studend add sex varchar(2);

删除列：

Alter talbe 表名 drop column 列名;

Alter table studend drop column sex;