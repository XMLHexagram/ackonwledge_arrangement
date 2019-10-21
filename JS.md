1.  ```html
    <script scr = "javascript.js"><script/>
    ``` 
    调用外部的javascript
2. 显示数据
    * document.write()
        * 如果在文档已经加载玩之后执行(通过函数调用)document.write，整个HTML页面都将被覆盖
    * window.alert() 弹出警告框
    * innerHTML
        * document.getElementById("*id*").innerHTML = "*sth*"
        * 通过Id定位元素，并修改HTML内容
    * console.log() 写入控制台
        * 在浏览器里按F12进入控制台查看
3. 变量
    * 通过var定义变量
4. 函数  
    ```js
        function temp(a,b) {
            return a*b
        }
    ```
    