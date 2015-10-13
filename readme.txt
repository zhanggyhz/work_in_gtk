今天学习了廖学风关于git的教程，学了两节。
Git is a distributed version control system.
Git is free software distributed under the GPL
git log --pretty=oneline 
git reset --hard HEAD^
git reset --hard c03b447335b41dc7cc44a9c9e4cb9f4c12c11ab5
git relog
git log
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

分布式版本系统的最大好处之一是在本地工作完全不需要考虑远程库的存在，也就是有没有联网都可以正常工作，而SVN在没有联网的时候是拒绝干活的！当有网络的时候，再把本地提交推送一下就完成了同步，真是太方便了！
Creating a new branch is quick.
Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

Creating a new branch is quick.

<<<<<<< HEAD
Creating a new branch is quick & simple.
=======
查看分支 git branch 
创建分支 git  branch  <name>
切换分支 git checkout <name>
创建加切换分支 git checkout -b <name>
合并某分支到当前分支 git merge <name>
删除分支 ：git branch -d <name>
Creating a new branch 'feature1'
>>>>>>> feature1
Creating a new branch is quick and simple.
