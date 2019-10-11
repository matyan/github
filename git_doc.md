# create repo
- $git init

- $git log

- $git reset --hard HEAD^/(HEAD~1)
- $git reset --hard <commit id>
- $git reflog

> working directory
> repository
---

git checkout --<filename>
- 未add则工作区中的filename恢复到和版本库一致
- add之后有修改则恢复到和暂存区一致

---
修改后并且add到暂存区
git reset HEAD <filename>
将修改后的文件退后到工作区

---
误删工作区文件，可通过
git checkout --<filename>进行恢复

# 远程仓库
1.设置ssh
$ssh-keygen -t rsa -C "erwei.yan@autofreetech.com"
会在.ssh目录下生成id_rsa（私钥）和id_rsa.pub（公钥）两个文件
登录GitHub，将id_rsa.pub添加到公钥区
在GitHub上建立仓库
$git remote add origin git@github.com:<账户名>/<仓库名>.git

即可将本地与远程库关联起来
$git push -u origin master
将本地仓库内容推送到远程库
$git push origin master

///////
第二种直接clone远程库
git clone git@github.com:matyan/github.git

////////////////
创建分支
git checkout -b dev/
git switch -c dev
合并指定分支到当前分支
git merge dev

删除分支
git branch -d dev


//////////////////
冲突解决
修改后再添加提交


合并分支非fast forward模式
git merge --no-off -m"commit" dev


/////
git stash
git stash list
git stash apply stash@{0}
git stash drop
//
git stash pop

////////////////
cherry-pick
git cherry-pick <commit>
合并指定commit节点

git branch -D <name>
删除一个没有被合并过的分支

///
查看远程库
git remote

推送到指定分支
git push origin master
git push origin dev


clone远程分支
git clone <>
clone master分支

clone特定分支
git checkout -b dev origin/dev


git branch --set-upstream-to <branch-name> origin/<branch-name>
远程分支与本地分支建立联系


git tag v1.0








