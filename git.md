## git上传包提交时出现：Please tell me who you are.
```
解决方法：在命令行中执行
git config --global user.email "你的邮箱"
git config --global user.name "你的名字"

输入完后再接着执行git commit "注释"
```

4.创建分支
在哪个分上使用git branch 创建分支就是从这个分支上复制一个新的副本,每一个分支都是独立的,互不干扰
```
git branch 查看分支 => * master 默认在主分支上面
git branch branchName 创建分支 例子:git branch dev =>

dev
* master

git branch branchName -D 删除分支
```

5.切换分支
```
git checkout branchName 
```
6.合并分支
```shell
git merge <oterBranch>
```
