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
