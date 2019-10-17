0. important commands:
    * select 提取数据
    * update 更新数据
    * delete
    * insert into 插入新数据
    * create database
    * alter database 修改数据库
    * create table
    * alter table 变更(改变)数据表
    * drop table 删除数据表
    * create index 创建索引(索引键)
    * drop index 
1. Basic Commands:
    *show databases;
    set names utf8;
    use *database*;
2. select:
    * SELECT *column_name,column_name* FROM *table_name* WHERE *column_name operator value* column：柱,栏,列
    * select * from *table_name* 显示数据表中的所有数据
    * SELECT DISTINCT(distinct:不同):
        * 仅仅返回不同的值
        * Select Distinct coutry(列) From *table_name*
    * WHERE:
        * Select * From *table_name* Where *id=1 or coutry='CN'*
        * =  <>  <  >=  <=  Between Like(%,_) In And Or
3. 