# Git ---- 分布式版本管理工具  
本文参考廖雪峰老师的[git教程](https://www.liaoxuefeng.com/wiki/896043488029600),用于记录自己的学习过程
* ## 概念  
------------------------
Git是windows、Linux、mac上的一个软件，用于软件开发过程中的版本管理。它是分布式的。每个人的电脑都可以用于一个完整的仓库。而仓库就是存放代码的地方。 

1、分布式  

<img src="./images/0.jpg" width="300">  

2、集中式  
<img src="./images/0 (1).jpg" width="300">  

---------------------------------------------------------------------
* ## Git相关术语
----------------------
> 工作区(work derectory)      ----- 即本地文件夹  
> 版本库                      ----- 包括暂存区和master分支等  
> 暂存区                       ----- git add命令后的文件存放点  
> master分支                   ----- 主分支  
> HEAD                          ----- 指向当前分支的指针  

------------------------------
### 相关参考 [传送门](https://www.liaoxuefeng.com/wiki/896043488029600/897271968352576)
<img src="./images/1.jpg">
---------------------------------------------------------------------
* ## 常用命令
------------------
```   
git clone [url/ ssh]  --- 克隆仓库   

git init   --- 初始化仓库   

git add [name]   --- 添加文件到暂存区  

git add .        --- 添加所有文件到暂存区   git add *.html   --- 添加某种后缀名的所有文件，以html文件为例   

git commit -m [tip]   --- 提交到当前分支  

git remote origin master --- 将本地仓库关联到远程仓库  
origin 为远程仓库的默认名称  

git push -u origin master  --- 将当前分支推送到远程仓库的master分支 

```
* ## 版本撤销与文件删除恢复
```
git log    --- 历史版本列表  

git status --- 查看工作区状态  

git diff   --- 查看工作区与版本库(暂存区和master)有无区别  

git log    --- 提交记录(最近提交的三条记录)

git reflog --- 执行命令记录(提交的历史操作记录)  

git reset  --- 版本回退 (版本回退)  

git reset HEAD []  --- 撤销暂存区修改  

git rm  [name]   --- 删除文件  

1.如果你用的rm删除文件，那就相当于只删除了工作区的文件，如果想要恢复，直接用git  checkout -- <file>就可以   
2.如果你用的是git rm删除文件，那就相当于不仅删除了文件，而且还添加到了暂存区，需要先git reset HEAD <file>，然后再git checkout -- <file> 3.如果你想彻底把版本库的删除掉，先git rm，再git commit 就ok了  
```
* ## 分支管理
```
git checkout  -- [name]     --- 撤销工作区修改  

git checkout  [name]   --- 切换分支 

git checkout -b [name]  --- 创建并切换分支  

git branch   --- 列出所有分支  

git branch -d [name] --- 删除分支  

git branch [name]   --- 创建分支  

git merge [name] --- 合并分支 

```
* ## 其它命令
```
git stash  --- 保存当前状态  

git stash --- 查看状态列表    

git stash drop  --- 删除保存的状态 

git stash pop   --- 恢复工作区并删除保存的状态

git pull    ---拉取  

```
