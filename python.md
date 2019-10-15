0. ``` 
   在python中使用该文件头，指定路径(linux)和指定utf-8编码:
   #!/usr/bin/env python 
   # -*- coding: utf-8 -*- 
   ```

1. print(r'''*sth*''') 可以预格式化内容,参数r将会忽略转义字符
2. **常用数据类型:**
   * list = []
        * 从0开始计数，倒数第一个是-1
        * list.append() 追加元素到末尾
        * list.insert(*poision*,*元素*) 在指定位置(索引)添加元素
        * list.pop() 删除元素
        * list [ *poision* ] = *sth* 直接赋值
   * tuple = () 
        * 
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
   1. 切片(Slice)
      * list[ 0:3 ] 从0开始取，到3为止。也就是会取出list[ 0 ],list[ 1 ],list[ 2 ]
      * list[ -2: ] 会取出list[ -2 ],list[ -1 ] 
      * list[ -2,-1 ] 只会取出list[ -2 ]
      * list[ :10:2 ] 前十个数字，每隔两个取一个
      * tuple和字符串也可以切片!!!切片后还是自己本生的数据类型
   2. 迭代(Iteration)
      * ```from collections import Iterable```
        ```isinstance('sth',Iterable)``` 判断sth是否可迭代，返回True就是可以
      * dict默认迭代key。
         * 使用```for value in dict.value()``` ```for key,value in dict.items()```指定迭代对象 
      * ```for i,value in enumerate(列举) ([])``` 同时迭代索引和元素本身
      * ```for x,y in [(1,1),(2,2),(3,3)]``` 
   3. 列表生成式(List Comprehensions) 
      * ```[x * x for x in range(1,11)]```
      * ```[x * x for x in range(1,11) if x % 2 = 0]``` 取1到10以内的所有偶数的平方
      * ```[m + n for m in 'ABC' for n in 'XYZ']``` 可以生成全排列哦
      * ```[key + '=' + value for key,value in dict.items() ]```
         * 前半段实际上是通过+和''组合出一个字符串
         * 后半段是同时迭代dict的key和value  
      * ```[s.lower() for string in List]``` 把List里面字符串中的大写字母转化成小写字母
   4. 生成器(generator)
      * ```generator = (x * x for x in range(10))```
      * 可以通过next(*generator*)调用下一个元素，当没有更多元素时，抛出```StopIteration```错误
      * 一般通过循环来调用*generator*：
         ```python
         for n in generator:
             print(n)
         ```
      * **An Important Warning(Tip):**
         ```python
         a , b = b , a + b
         ```
         相当于：
         ```python
            tuple_temp = (b , a + b)
            a = tuple_temp(0)
            b = tuple_temp(1)
         ```
      * 使用```yield```关键字，将函数变成生成器(创建生成器) 
      * 请注意yield关键字,导致的特殊运行方式(生成器的特殊运行方式)
         * 遇到yield时返回，下一次执行从上次的yield语句后开始执行
      * 可以通过捕获错误的方式，实现返回值 
   5. 迭代器(Iterator)
      ```python
      from collections import Iterator
      isinstance(sth,Iterator)
      ```
      * 可迭代(Iterable)和迭代器(Iteration)是不同的，迭代器一定可迭代，可迭代不一定是迭代器
      * 可迭代,但不是迭代器：list,dict,str,tuple,set
      * 是迭代器:generator
      * 迭代器可以使用next()
      * 使用```iter()```将Iterable转换成Iteration
      * Iterator是一个数据流(甚至可以无限大)，是一个惰性计算数列
   6. 