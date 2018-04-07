### git fetch <远程主机名> 取回远程主机的所有更新
### git fetch <远程主机名> <分支名> 取回远程主机的特定更新
### git fetch origin master 取回远程主机的master分支更新

### 取回远程主机的更新以后，可以在它的基础上，使用git checkout命令创建一个新的分支(此操作会自动确立分支关联关系)
- git checkout -b newBrach origin/master 上面命令表示，在origin/master的基础上，创建一个新分支

### 此外，也可以使用git merge命令或者git rebase命令，在本地分支上合并远程分支
- git merge origin/master 或者 git rebase origin/master 上面命令表示在当前分支上，合并origin/master

### git pull = git fetch + merge
### 当前分支没有关联分支的情况下使用git pull 会报错 

### git pull命令的作用是，取回远程主机某个分支的更新，再与本地的指定分支合并。它的完整格式稍稍有点复杂。
- git pull <远程主机名> <远程分支名>:<本地分支名>
- git pull origin next:master 取回origin主机的next分支，与本地的master分支合并
- git pull origin next  远程分支next与当前分支合并 等同于git fetch origin&& git merge origin/next(此操作会自动确立分支关联关系)

