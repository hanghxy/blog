# 使用 Git 操作SVN项目：
```bash
$ git svn clone http://svn.360buy-develop.com/repos1/O2O/m-html/branches/webapp/v1.1/html  --克隆项目到本地
$ git svn fetch  获取最新的数据
$ git svn rebase 会在获取之后在本地进行更新，它会拉取服务器上所有最新的改变，再次基础上衍合你的修改

$ git commit -am 'Adding git-svn instructions to the README'  提交代码到暂存区
$ git svn dcommit 提交到服务器

$ git show-ref 查看所有引用的全名

$ git branch opera 创建一个新分支
$ git branch -b opera 创建一个新分支
$ git checkout opera 切换分支
$ git branch -d test  删除一个分支

$ git rebase  用于把一个分支的修改合并到当前分支。

$ git checkout -f  强制还原工作区
```
