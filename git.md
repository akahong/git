# Git Operation

## 创建版本库(必须在需要创建版本库的文件下)：
``` 
git init
```
## 查看文件夹下的所有文件：
ls -a
## 定义提交者的username
git config —-global user.name “xxxx”
## 定义提交者的uesremail
git config —-global user.email “xxxx”
## 查看定义提交者的信息是否已创建成功
git config user.name
git config user.email

新建文件
touch 文件名（如：1.py）

查看状态
git status

查看状态的简写
git status -s

添加指定文件
git add 文件名

添加所有文件
git add .

提交文件
git commit -m  “ Xxx”

添加并提交已存在的文件
git commit -am “xxxx”

提交到已存在的commit且不修改commit的评论
git commit —-amend —-no-edit

查看修改记录
git log

以一行的形式显示修改纪录
git log —-online

以图形的形势显示log
git log —-online —-graph

查看不同（查看unstage状态和之前commit状态的区别）
git diff

查看不同（查看状态和之前commit状态的区别）
git diff —cached

查看不同（查看stage状态和之前unstage状态的区别）
git diff HEAD

回到过去（由stage状态回到unstage（modify）状态）
git reset 文件名

回到过去（由commit回到add之前）
git reset —－hard HEAD

回到上一个已修改的状态
git reset -－hard HEAD^

回到上两个已修改的状态(以此类推)
git reset -－hard HEAD^^
或
git reset -－hard HEAD~2

回到指定的过去
git reset -－hard  commit的id号

查看未来的id
git reflag

回到未来
git reset -－hard  未来commit的id号
git reset -－hard  未来的指针

回到过去（单个文件回到过去）
git checkout commit的id —- 回到过去的文件名

checkout和reset区别：
reset创造新的未来
checkout 回到过去的某个点，修改后，其他的文档不变

创建分支
git branch 分支名

创建分支并将指针移到分支上
git checkout -b 分支名

查看分支
git branch

切换分支
git checkout 分支名

删除分支
git branch -d 分支名

将分支推到master
git merge —-no-ff -m “xxx” 分支名


merge分支冲突

基于分支修改主分支
git rebase 分支名

继续执行rebase
git rebase —-continue

忽略rebase提示
git rebase —-skip

放弃rebase操作
git rebase —-abort

放入缓存区（已经add）
git stash


回到缓存区
git stash pop

将文件与Github关联
git remote add origin https://github.com/akahong/mook.git

将文件推到github
git push -u origin master


将github文件克隆到本地
git clone origin https://github.com/akahong/mook.git

















