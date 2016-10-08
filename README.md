![git command](git.jpg) 
## 配置
- git邮箱和账号
```
git config --global user.name '用户名'
git config --global user.email '邮箱'
```
- 查看配置
```
git config --list
```
##  创建目录
```
mkdir 目录的名字
```
## 改变目录
```
cd ..
```
# 本地文件夹操作（locals)
##  git init 
```
git init
```
> 初始化本地仓库，表示当前文件夹归git所管理

## echo可以输入内容并且创建文件 
```
echo hello > index.txt
```

## 查看文件的内容
```
cat 文件名
```
## 创建文件
```
touch 文件名
```
## 编辑
```
vi index.txt
```

> 先按i键 进入insert模式 更改后按esc， :wq退出

## 追加内容
```
echo world >> index.txt
```
> 一个大于号表示清空并写入，两个大于号表示追加内容

## 将内容追加到暂存区中
```
git add .   /git add -A / git add 文件名
```

## 提交到历史区中
```
git commit -m "对于本次提交的描述内容"
```

## 查看版本库日志
```
git log --oneline
```
## 比较不同
- 默认比较的是工作区和暂存区的不同
```
git diff 
```
- 工作区和版本库
```
git diff master
```
- 暂存区和版本库
```
git diff --cached
``` 
## 不能用于某个文件的首次提交
```
git add 
git commit -m
git commit -a -m 'write second'
```

## 拉回本次的add内容
```
git reset HEAD index.txt
```
## 将暂存区的内容覆盖掉工作区
```
git checkout index.txt
```
> 暂存区中没有会从历史区拉回来

## 回滚
- 用历史区覆盖掉工作区
```
git reset --hard 版本号
```
## 查看历史版本
```
git reflog
```

## 回滚指定回滚几个版本
```
git reset --hard HEAD^/HEAD~1
```

## 分支
- 创建分支
```
git branch 分支名字
```
- 切换分支
```
git checkout dev
```
- 查看分支
```
git branch
```
- 删除分支
```
git branch -d dev
```
## 即创建分支同时进入到分之中
```
git checkout -b dev

相当于下面俩句
git branch 分支名
git checkout 分知名
```
## 创建线上分支
```
git checkout -b gh-pages
```
## 在分支上进行开发
- 开发后切换到主分支上合并本次的开发
```
git merge dev  在主干分支上合并就要切换到主分支上
```
## 解决冲突
将<<<< ====>>>>>删除保留想要的再次提交
再次add commit 生成合并后的版本
## 查看族谱（以图像形式显示并显示分支）
```
git log --graph --decorate
```
## 如果正在开发时却换分支 要保证工作区和暂存区都为干净的 否则不让切换

```
git stash  保留  用历史区覆盖暂存区和工作区
```

## 查看保存的内容
```
git stash list  查看保存目录

git stash apply 应用保留

git stash drop 丢掉保留

git stash pop
```
## rebase 变基
- rebase 和merge的区别 
- 更改了合并的线条
- 不会产生新的提交，在当次提交上演绎分支上的提交，最终合并成了一个提交
## cherry-pick 挑选精选
```
git cherry-pick 当前分支的版本号
```
#origin
添加本地仓库到远程仓库
```
git remote add origin 仓库地址
```
## 查看远程仓库地址
```
git remote -v
```
## 删除远程仓库
```
git remote rm origin
```
## 推送到远程仓库
```
git push -u origin master  第一次提交增加了-u 下一次可以直接使用git push
```
## 在正常提交之前要使用忽略文件，忽略掉不想提交的文件
```
touch .gitignore

添加如下内容

.idea
.DS_Store
node_modules/
```
## 将远程仓的资源拉取到本地
- 拉取最新代码
```
git pull
```
## github上的fork
- fork只能fork一次 拉取过来的仓库 原来被fork的仓库改变了 本地仓库不变

##git详细教程
[**git廖雪峰教程**](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000) 

