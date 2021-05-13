
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
### commit之后发现有错误,想要修改对应的文件，然后进行覆盖提交，不生成新的commit记录
    修改完对应的文件
    git add .
    git commit --amend -m '覆盖式提交'
### commit之后发现错误，想完全撤销本次操作
    git reset --hard HEAD~1
    ps:这样上一次的提交记录会消失，同时'覆盖式提交'这次提交的代码，以及之后修改的代码会完全消失。
    代码会变成'覆盖式提交'上个分支的代码，请慎用此命令
### commit之后，撤销这次提交，保留工作目录，改动保存在暂存区
    git reset --soft HEAD~1
    然后修改完错误的地方后再次提交
    