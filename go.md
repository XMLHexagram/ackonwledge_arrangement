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
2. 变量
    * var *name* int = 100
    * *name* := 100
    * a,b = b,a
    * 匿名变量 **_**
        * 用于占位，避免必须用变量接受每一个返回值
    * bool型必须显式的转换成数字(0,1),数字也必须显式转换成bool型
    * 字符串
        * 拼接+ +=
        * 通过 `` 实现嵌入多行字符串，并且会保留原格式
3. 类型转换
    * go语言没有隐式类型转换
    * 必须使用类似于 int(*sth*)的强制转换
4. 常量
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
            )
            ``` 
        Sunday = 0, Monday = 1, etc

5. 指针 
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
