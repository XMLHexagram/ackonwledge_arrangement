0. ``` 
   在python中使用该文件头，指定路径(linux)和指定utf-8编码:
   #!/usr/bin/env python 
   # -*- coding: utf-8 -*- 
   ```

1. print(r'''*sth*''') 可以预格式化内容,参数r将会忽略转义字符
2. **常用数据类型:**
   * list = []
**tuple,dict,set均不可在元素中使用可变对象**
**及以不可变对象作为key**
   * tuple = () 
**key不允许重复**
   * dict = {}
        * dict = {'*key*:*value*,'*key*:*value*,*key*:*value*}
        * dict[ *existed_key* ] = *new_vlaue* 
        * 判断key是否在dict中
            * '*key*' in dict 返回True or False
            * dict.get('key',num) 如果key不存在返回False or num
        * dict.pop('key') 删除key及其value
   * set =([ *key,key,key,etc* ])
        * []作为list提供输入
        * 用法: s = set([])
        * s.add(*key*) 可以添加元素
        * s.remove(*key*)
        * s1 & s2 交集
        * s1 | s2 并集
4. **函数:**
   ```
   def *name_of_function* ():
   return *a,b,c,etc*
   ```
   * return多个值时,返回值是一个tuple
   1. 必选参数
   2. 默认参数 ```def example (x = 10):```
   3. 可变参数 ```def example (*args):```
      * 在list或tuple前面加一个*，把list和tuple变成可变参数
   4. 关键字参数 ```def emample (**kw):```(key word)
      * 使用方法 ```example(key='value'，city='Hangzhou')```
      * 也可以先组装出字典，再通过**dict传进去
   5. 命名关键字参数 ```def example (temp,temp,*,key=value,key)``` 
      * 可以限定传入的key:value中的key的名称
      * 可以有缺省值
   **参数的定义顺序必须是：必选参数，默认参数，可变参数，命名关键字参数，关键字参数**
   * 参数不同形式组合使用时，一定要慎重，组合过于复杂，将导致函数接口难以理解
   * ```func(*args,**kw)```
      * *args是可变参数，接收一个tuple
      * **kw是关键字参数，接收一个dict
   6. 递归函数
5. **高级特性:**
   1. 切片
      * list[ 0:3 ] 从0开始取，到3为止。也就是会取出list[ 0 ],list[ 1 ],list[ 2 ]
      * list[ -2: ] 会取出list[ -2 ],list[ -1 ] 
      * list[ -2,-1 ] 只会取出list[ -2 ]
      * list[ :10:2 ] 前十个数字，每隔两个取一个
      * tuple和字符串也可以切片!!!切片后还是自己本生的数据类型
   2. 迭代
      * ```from collections import Iterable```
        ```isinstance('sth',Iterable)``` 判断sth是否可迭代，返回True就是可以
      * dict默认迭代key。
         * 使用```for value in dict.value()``` ```for key,value in dict.items()```指定迭代对象 
      * ```for i,value in enumerate(列举) ([])``` 同时迭代索引和元素本身
      * ```for x,y in [(1,1),(2,2),(3,3)]``` 
   3. 列表生成式 