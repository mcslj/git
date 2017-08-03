# 03-Git初次使用

Git笔记
# 使用lantern 翻墙 设置全局代理
##1, 当安装完 Git 应该做的第一件事就是设置你的用户名称与邮件地址。 这样做很重要，因为每一个 Git 的提交都会使用这些信息，并且它会写入到你的每一次提交中，不可更改： 
$ git config --global user.name "John Doe"  
$ git config --global user.email johndoe@example.com

## 查看用户名和邮箱
$ git config user.name

$ git config user.email

##2, 设置文本编辑器 $ git config --global core.editor emacs

## 在空文件夹下设git置本地仓库 $ git init

## 创建文件夹 $ mkdir pt1  创建文件 $ touch readme.txt 

## 把文件加入暂存 $ git add readme.txt

## 提交 $ git commit -m '第一次提交'

## 加入tag $ git tag v1.0

## 查看所有tag $ git tag

## 显示tag所属 $ git show v1.0

## 删除tag:git tag -d v1.0

## 返回到那个版本$:git reset --hard 139dcfaa558e3276b30b6b2e5cbbb9c00bbdca96
   使用$:Git log命令查看所有的历史版本，获取某个历史版本的id，假设查到历史版本的id是   139dcfaa558e3276b30b6b2e5cbbb9c00bbdca96。

## 推送到远程分支 git push -f origin master

## 设置秘钥:ssh-keygen -t rsa -C "mc92slj@gmail.com"

## 把本地git仓库勾连远程服务器 $ git remote add origin https://github.com/mcslj/pt3.git
## 把修改提交到远程仓库 $ git push -u origin master  $ git push origin master  
   输入GitHub 用户名 mcslj
   输入GitHub 密码 mc92slj@@

## 删除本地git仓库先删 .git 文件 $ rm -rf .git

## 从已有的分支创建新的分支(如从master分支),创建一个dev分支 $ git checkout -b dev

## 创建完可以查看一下,分支已经切换到dev $ git branch


## 建立本地到上游（远端）仓的链接 --这样代码才能提交上去 $ git branch --set-upstream-to=origin/dev 

## 取消对master的跟踪 $ git branch --unset-upstream master

## 切换分支 $ git checkout master  

## 合并分支 $ git merge dev

## 查看本地分支 $git branch  查看远程分支 $ git branch -a

## 把分支推到远程仓库 $ git push origin dve

## 删除本地分支  $ git branch -d dve

## 删除远程分支$ git branch -r -d origin/branch-name

#分支总结
## 新创建的分支dev的内容跟master里的内容一样只是互不干扰. dev分支可以进行修补 测试 而且不干扰mashter分支的正常运作完成后可以合并到master分支里.
