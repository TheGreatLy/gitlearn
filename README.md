# gitlearn
#### 将git仓库克隆下来

`git clone xxxx`

#### 创建远程分支，并查看远程分支和本地分支

- 创建，github仓库内new branch
- 查看 `git branch -a`

#### 创建本地分支

`git branch branchname`

​        对于协同开发的项目而言，一般**不在master直接提交和修改代码**，因为master分支记录了整个项目从开始到结束的代码，它应该总是**稳定的**，对于我们未经过测试的不确定的代码文件，如果直接在master分支进行修改和提交，将会引入很多不确定的漏洞。

所以，我们对于每个项目来说，应该在master主分支上创建许多远程功能分支。然后每个人负责维护代码在分支上。

然后我们创建本地分支，将本地分支与远程分支相关联，待本分支上的内容测试结束后再合并到master分支上。

创建完毕后，我们在本地仓库中切换到新建的本地分支中 `git checkout branchname`

代码修改完毕后如何将本地分支的代码推到远程分支中？

`git add .`

`git commit -m 'desc'`

**第一次push：**

`git push -u origin brachname:远程分支name`

**非第一次push:**

`git push origin brachname:远程分支name`

分支代码测试没问题之后，合并到master

`git checkout master`

`git merge branchname`

`git push`将代码推到远程主分支仓库