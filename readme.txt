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
