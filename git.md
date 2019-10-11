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
12. git remote add origin git@github.com:lmx-Hexagram/ackonwledge_arrangement.git
13. 