
1. git config --global user.name "Hexagram"
   git config --global user.email "1471685806@qq.com"
   * 登记名字和邮箱以使用git

2. git init 初始化
3. git status
4. git diff
   * git diff HEAD -- *file* 查看*file*在工作区和版本库里最新版本的区别
5. git add
6. git commit -m
7. git log
8. git reset --hard HEAD^
    * git reset HEAD *file* 把暂存区的修改退回的工作区
9. git reflog 记录了使用的每一次命令
10.  git checkout -- *file* 丢弃工作区的修改
    * 按情况回到**版本库**或者**暂存区**的状态
    * 实质是使用已存文件替换工作区的版本
11. git reset HEAD *file*
12. git rm *file*  
> 连接到远程仓库:
13. ssh-keygen -t rsa -C "1471685806@qq.com"
    * 建立一个本地的ssh公钥和私钥，再把公钥丢到GitHub上
    * 建立时没有设置密码
14. git remote add origin git@github.com:lmx-Hexagram/ackonwledge_arrangement.git
    * git@github.com:用户名/仓库名.git
15. git push -u origin master
    * 第一次使用时需要用-u参数，使其在推送本地master分支的同时，把远程仓库和本地仓库联系起来，以简化以后的命令
    * git push origin master以后只要这样就可以了
16. git clone git@github.com:lmx-Hexagram/ackonwledge_arrangement.git
    * 从远程仓库克隆
    * git@github.com:用户名/仓库名.git
    * 也可以使用 git clone https://github.com/lmx-Hexagram/ackonwledge_arrangement.git
    * 也就是可以使用SSH和https两种协议
>以上是链接远程仓库的方法

