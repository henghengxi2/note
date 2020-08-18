# 基本概念

upstream/branch 源仓库分支，即上游，可简写为 -u

origin/branch 远程仓库分支，即镜像源，可简写为 -o

branch 本地仓库分支

<remote> 代表指向哪个服务器或者说仓库 origin upstream

<branch> 代表分支名称

master 创建仓库时的默认名称，并没有特殊含义

# 一、初始化仓库

1. git init: 在已有文件下 git init 仓库，然后 git add 对文件进行追踪
2. git clone: 在某个目录下克隆项目,创建镜像仓库

# 二、远程仓库

1. 追踪远程分支并在本地创建同名分支 git checkout --track <remote>/<branch>或者 git checkout -b <branch> origin/<branch>
2. 当本地分支已有时，又想本地分支跟踪上游某个分支 git branch -u <remote>/<branch>
3. 同步最新数据 git fetch <remote>
4. 推送当前分支提交内容到远程某个分支 git push <remote> <branch>或者
   git push origin branch(本地分支名):branch(远程分支名，已有或新创建)
5. 合并远程分支到当前分支 git merge <remote>/<branch>
6. 先 git fetch --all 同步最新数据， 然后 git branch -vv 查看所有本地分支追踪远程分支的对应情况
7. git pull 拉取本地分支对应的追踪分支数据并且自动合并
8. 删除远程分支 git push origin --delete <branch>(短暂时间内误删可恢复)或者 git push origin :<branch>
