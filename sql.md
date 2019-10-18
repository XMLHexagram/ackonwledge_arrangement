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
    * SELECT *column_name,column_name* FROM *table_name* WHERE *column_name operator value* 
    * column：柱,栏,列
    * select * from *table_name* 显示数据表中的所有数据
    * SELECT DISTINCT(distinct:不同):
        * 仅仅返回不同的值
        * Select Distinct coutry(列) From *table_name*
    * WHERE: **(定位)**
        * Select * From *table_name* Where *id=1 or coutry='CN'*
        * =  <>  <  >=  <=  Between Like(%,_) In And Or
    * ORDER BY(用于对结果集按照一个列或者多个列进行排序)
        * ORDER BY *column_name,column_name* ASC|DESC;
        * 默认按照升序(ASC)进行排序,可以用关键字DESC进行降序排序
        * ORDER BY 语句的添加位置和WHERE相同
3. INSERT INTO
    * 
    INSERTI INTO *table_name* *(column2,column2,column3,...)*
    VALUES (value1,value2,value3,...);
4. UPDATE
    * 
    UPDATE *table_name*
    SET *column1=value1,column2=value2,...*
    WHERE *some_column = some_value*;
    * Warning:一定要带上WHERE定位！！！
5. DELETE (删除行)
    * 
    DELETE FROM *table_name*
    WHERE *some_column = some_value*;
    * 特殊用法:DELETE * FROM *table_name*
        *删除表中所有行,但是保留结构,属性,索引不变 
