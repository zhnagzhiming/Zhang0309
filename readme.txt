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

新加一行
