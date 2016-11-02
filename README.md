##配置使用人的账号和邮箱
```
git config --global user.name ryanzhao1993
git config --global user.email ryanzhao1993@qq.com
git config --list 查看所有配置
```

##初始化git
```
git init
```

## 创建忽略文件
> .gitignore文件
```
.idea
node_modules
```

##编辑需要的文件
```
vim xxx
```

##本地3个区域
* 工作区
* 暂存区
* 历史区(版本库)

## 查看状态
```
git status
```
> 红色表示在工作区中
> 绿色代表在暂存区中

## 将文件从工作区加入到暂存区
```
git add <file>
git add .
git add -A
```

## 将文件从暂存区提交到历史区
```
git commit -m "commit msg"
```


## 查看版本库信息
```
git log
git log --oneline   //一行显示
```

##查看未来的版本
```
git reflog
```

## 比较代码差异
* 比较工作区和暂存区的区别
```
git diff
```

* 比较工作区和历史区的区别
```
git diff master
```

* 比较暂存区和历史区的区别
```
git diff --cached
```

## 从暂存区删除本次的add
```
git reset HEAD <file>
```

> 取消本次的add

## 从缓存区 从历史区将代码覆盖掉工作区
```
git checkout <file>
```

##回到过去
```
git reset --hard <commit_id>
git reset HEAD^^^^^^^
git reset HEAD~6
```


##分支
* 查看所有分支
```
git branch
```

* 创建分支
```
git branch <branch_name>
```

* 切换分支
```
git checkout <branch_name>
```

* 创建并切换
```
git checkout -b <branch_name>
```

* 删除分支
```
git branch -d <branch_name>
git branch -d <branch_name>
```

* 合并分支
```
git merge <branch_name>
```

> 在master上拉取一条branch，在branch上进行开发，开发后，在master上将代码进行合并
> 如果master上目前没有人开发，可以使用快转的方式，将我们的指针直接指向到分支的最新装态 fast-forward

* 解决冲突

> 去掉>>>>>> ========  <<<<<<< 保留需要的内容再次提交

* 合并
> git rebase 变基
> git cherry-pick 精选

* 显示结构
```
git log --graph --oneline --decorate
```


##远程仓库
* 添加远程仓库的连接
```
git remote add <alias> <github_url>
```
* 删除地址
```
git remote rm <alias>
```

* 查看远程仓库地址
```
git remote -v
```


## fork
> 把别人的项目原封不动的拷贝一份放置到自己的github上，只能fork一次

## 从github拉到本地
```
git clone <github_url> <dir_name>
```

## 项目添加callorbrators
> settings-> callorbrators -> add

## 在github上部署静态页
> 需要将特定的内容push到github上的gh-pages分支上
> branch名字必须是gh-pages

- 创建一个gh-pages的分支,并切换到该分支
```
git checkout -b gh-pages
```

- 将代码commit 到这个分支上
```
git add .
git commit -m 'commit msg'
```

- 连接远程仓库和本地仓库
```
git remote add <alias> <github_url>
```

- 将gh-pages分支代码推送到远程仓库上
```
git push <alias> gh-pages
```

 








