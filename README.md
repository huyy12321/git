
### git新建文件，添加到本地
    git add .
### git提交文件
    git commit -m '测试'
### git从远程拉取代码
    git pull
### git提交本地代码
    git push
### git查看当前分支
    git branch
### git切换分支
    git checkout
    
## 工作空间：最开始写的代码都是在工作空间 working Tree
## 暂存区域：add之后，文件会保存在这里 index/Stage
## 提交记录：commit后，文件会保存在这 Repository

### commit之后发现有错误,想要修改对应的文件，然后进行覆盖提交，不生成新的commit记录
    修改完对应的文件
    git add .
    git commit --amend -m '覆盖式提交'
### commit之后发现错误，想完全撤销本次操作,三个区域的代码都会回到目标分支的状态
    git reset --hard HEAD~1
    ps:这样上一次的提交记录会消失，同时'覆盖式提交'这次提交的代码，以及之后修改的代码会完全消失。
    代码会变成'覆盖式提交'上个分支的代码，请慎用此命令
### commit之后，撤销这次提交，保留工作空间，有错误的commit代码会保存在暂存区域
    git reset --soft HEAD~1
    然后修改完错误的地方后再次提交
### 撤销提交，把所有的改动都放在工作空间
    git reset --mixed HEAD~1 (不加--参数的时候默认这种)
### 刚push后，发现提交的有问题，想要修改远程的分支
    本地先reset，修改完后push到远程分支
    git reset HEAD~1
    git push --force
    ps: --force会进行覆盖，如果这中间其他人提交了代码，也会被覆盖
### 线上回退到某个版本
    git reset --hard HEAD~n n为目标记录
    git push --force
    ps:回退版本到目前版本之间的代码会不见,记得备份

    