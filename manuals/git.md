# Git常用指南
> 可以在git官网上下载到[Git指南](https://git-scm.com/book/en/v2)


## 配置用户信息

> global 文件

		$ git config --global user.name username
		$ git config --global user.email user@example.com

		$ git config --list 查看已配置信息


## Git 状态

+ Git仓库

+ 工作目录

+ 暂存


## Git 基础使用

1. 创建版本库   `git init` or 'git clone respositoriyUrl'

2. 添加文件到暂存  `git add [dir | file]`

3. 删除当前修改  `git checkout [dir | file]`

4. 添加忽略文件（如项目的调试中间文件等）
> 通过编辑.gitignore文件 如向文件中添加  *.[oa]等

5. 查看文件的具体修改
	+ 查看当前的修改与上一次add到暂存中的修改的差别  `git diff`
	
	+ 查看暂存中与上一次commit的区别 `git diff --staged`
	
6. 提交更新
	+ 只是将暂存里面的修改进行提交  `git commit -m message`
	
	+ 将最新的修改连同暂存一起提交  `git commit -a -m message`
	
	+ 补充提交而不是生成新一次提交  `git commit --amend`
	
7. 查看提交历史 `git log`  
> --stat 在每次提交的下面列出所有被修改过的文件、有多少文件被修改了以及被修改过 的文件的哪些行被移除或是添加了


## 远程仓库
1. 查看远程仓库信息  `git remote -v`

2. 添加远程仓库  `git remote add [respositoryName] respositoryUrl`


## Git 别名
		git config --global alias.name command
		
		git config --global alias.unstage 'reset HEAD --'
		
		查看上一次提交
		git config --global alias.last 'log -1 HEAD'


## Git 分支

1. 创建分支 `git branch branchName`

2. 切换分支 `git checkout branchName` && 创建并切换分支 `git chechout -b branchName`

3. 删除分支 `git branch -d branchName`

4. 合并分支
	1. 切换到被合并的分支
	
	2. `git merge branchWantToMergeIn`
	
	+ 合并错误
		+ <<<<< 当前分支里面的内容 ====== 与当前产生冲突的内容 >>>>>
		
		+ 手动解决掉冲突（包括冲突内容和 > < =）

		+ `git add .`进行提交
		
5. 提交分支 `git push remoteBranch`
> 创建本地分支并同步到远程仓库 `git push --set-upstream origin branchName`

6. 拉取分支
	1. `git pull` 同时对本地目录和本地的仓库进行同步
	
	2. `git fecht` 只是本地仓库同步，需要手动merge到目录（recommend）


## 使用ssh进行提交
	[参考](https://www.cnblogs.com/ldq2016/p/7418206.html)

#### Git与其它管理方法的区别

