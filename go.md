
0.  {}的"{"不能换行
1. 
    * ```go
        package main

        import (
            "fmt"
        )

        func main() {
            fmt.Println("Hello Go!")
        } 
        ```
    * package(创建包)
        * 用一目录下的同级文件属于同一个包
        * 包名可以和目录名不同
        * main包有且只有一个
    * import
        * 导入包
        * 导入的包必须使用
2.  变量
    * 首字母大写为导出变量，可以被其它包调用
    * var *name* int = 100
    * *name* := 100
    * a,b = b,a
    * 匿名变量 **_**
        * 用于占位，避免必须用变量接受每一个返回值
    * bool型必须显式的转换成数字(0,1),数字也必须显式转换成bool型
    * 字符串
        * 拼接+ +=
        * 通过 `` 实现嵌入多行字符串，并且会保留原格式
3.  运算符
    * 主要运j算符基本与C语言相同 
    * 只允许使用a++,且**不允许:** a = a++ 
4.  类型转换
    * go语言没有隐式类型转换
    * 必须使用类似于 int(*sth*)的强制转换
5.  常量
    * const name type = value
        * const pi = 3.14
        * const pi int = 3.14
    * iota常量生成器
        * ```go
            type Weekday int

            const (
                Sunday Weekday = iota
                Monday
                Tuseday
                Wednesday
                Thursday
                Friday
                Saturday
            )j
            ``` 
        Sunday = 0, Monday = 1, etc
        * iota在每一次const出现时被重置为零，并且每新一行会自增1

6.  指针 
    * 与C语言指针类似
     ```go    
        package main
        import "fmt"
        // 交换函数
        func swap(a, b *int) {
            // 取a指针的值, 赋给临时变量t
            t := *a
            // 取b指针的值, 赋给a指针指向的变量
            *a = *b
           // 将a指针的值赋给b指针指向的变量
            *b = t
        }
        func main() {
        // 准备两个变量, 赋值1和2
            x, y := 1, 2
            // 交换变量值
            swap(&x, &y)
            // 输出变量值
            fmt.Println(x, y)
    }
    ``` 
    * 经典例子,在c里面也是一样的

7.  流程控制语句
    1. 条件语句
        * ```go
            if bool_value {
                /*True*/
            } else {
                /*False*/
            }
            ```
    2. 循环语句
        * 和C语言的for相同
            ```go 
                for init; condition; post { }
            ```
        * 和C语言的while相同
            ```go
                for condition { }
            ``` 
        * 和C语言的 ```for (;;) {}```相同
            ```go
                for { }
            ```
        * go语言for循环的range格式,可以像Python一样迭代,slice,map,数组,字符串,etc
            * ```go
                for key, value := range oldMap {
                    newMap[key] = value
                }
                ```
            * example 
            ```go
                number := [6]int{1,2,3,4,5} //没赋值默认是0
                for i, x:= range number {
                    fmt.Printf("第%d位的值 = %d\n",i,x)
                }
            ```
8.  函数
    * 定义
    ```go
        func function_name( [parameter list] ) [return type] {
            //函数体
        }
    ```
    * ```go
        func max(num1,num2 int) int {
            var result int

            if num1>num2 {
                result = num1
            } else {
                result = num2
            }
            return result
        }
        ``` 
    * 可以```return x,y```返回多个值
    * 函数作为另一个函数的实参
    * 闭包
    * 方法
9.  数组
    * ```go
        var variable_name [SIZE] variable_type {value,value,value,etc}
        ```
    * {}内value个数不得多于[ size ]中的size数字，可以少于(自动初始化)
    * []内可以没有数字,会自动匹配
    * 向函数传递数组参数
    * 高维数组
10.  结构体 