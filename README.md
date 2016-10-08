## 配置
- 的git邮箱和账号
```
git config --global user.name '用户名'
git config --global user.email '邮箱'
```
- 查看配置
git config --list
##  创建目录
```
mkdir 目录的名字
```
## 改变目录
```
cd ..
```
# locals
##  git init 
初始化本地仓库，表示当前文件夹归git所管理

## echo可以输入内容并且创建文件 
```
echo hello > index.txt
```

## 查看文件的内容
```
cat 文件名
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
git commit 
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