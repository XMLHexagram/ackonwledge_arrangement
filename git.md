1. git init 初始化
2. git status
3. git diff
   * git diff HEAD -- *file* 查看*file*在工作区和版本库里最新版本的区别
4. git add
5. git commit -m
6. git log
7. git reset --hard HEAD^
    * git reset HEAD *file* 把暂存区的修改退回的工作区
8. git reflog 记录了使用的每一次命令
9. git checkout -- *file* 丢弃工作区的修改
    * 按情况回到**版本库**或者**暂存区**的状态
    * 实质是使用已存文件替换工作区的版本
10. git reset HEAD *file*
11. git rm *file*
------------------------------------------------------------------------------
连接到远程仓库
12. ssh-keygen -t rsa -C "1471685806@qq.com"
    * 建立一个本地的ssh公钥和私钥，再把公钥丢到GitHub上
    * 建立时没有设置密码
13. git remote add origin git@github.com:lmx-Hexagram/ackonwledge_arrangement.git
    * git@github.com:用户名/仓库名.git
14. git push -u origin master
    * 第一次使用时需要用-u参数，使其在推送本地master分支的同时，把远程仓库和本地仓库联系起来，以简化以后的命令
    * git push origin master以后只要这样就可以了
------------------------------------------------------------------------------