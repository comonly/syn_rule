# syn_rule
本地仓库与远程仓库的同步方式，分支创建、维护、合并等

# 查看当前分支
当前分支前面有一个*  
$ git branch

# 创建分支
创建并切换分支  
$ git checkout -b dev  
相当于  
$ git branch dev  
$ git checkout dev  
远程同步创建的分支,将本地dev分支push到远程dev，没有远程dev会自动创建  
$ git push origin dev:dev

# 删除分支
删除本地dev分支  
$ git branch -d dev  
删除远程dev分支  
$ git push origin --delete dev

# 合并分支
合并指定分支到当前分支 包括分支的提交记录  
$ git merge dev  
合并指定分支到当前分支 包括分支的提交记录 包括本次提交的一次commit  
$ git merge --no-ff -m "merge with no-ff" dev