0. ``` 
   在python中使用该文件头，指定路径(linux)和指定utf-8编码:
   #!/usr/bin/env python 
   # -*- coding: utf-8 -*- 
   ```

1. print(r'''*sth*''') 可以预格式化内容,参数r将会忽略转义字符
2. 
3. 常用数据类型
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
4. 函数