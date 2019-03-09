初始化一个Git仓库，使用git init命令。
添加文件到Git仓库，分两步：
1.使用命令git add 文件名   ，注意，可反复多次使用，添加多个文件；
2.使用命令git commit -m“对文件修改的解释”  ，完成。
git status命令可以让我们时刻掌握仓库当前的状态
用git diff这个命令看看具体修改了什么内容

HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

用$ git reset --hard HEAD^回退到上个版本时，再想恢复到最新，就必须找到最新版本的的commit id。
Git提供了一个命令git reflog用来记录你的每一次命令

learngit文件夹就是一个工作区
工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，
还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD

每次修改，如果不用git add到暂存区，那就不会加入到commit中

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，
		第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。

7.16.17.18.19.20.24.29.30.41---先不看
学会git，学习全面的maven知识

2019.3.9测试行
0309测试分支结构，新建dev