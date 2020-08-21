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

9.配置参数
```shell
##  --global 可以不写,以后每次创建仓库都需要在配置一遍
## --global 加上后,以后所有项目默认都使用这两个参数
git config --global user.email "你的邮箱"
git config --global user.name "你的名字"
```
## 远程仓库
1.github 这个是免费托管代码的网站
[github](https://github.com/)

支持两种模式
-Publice 每个人都可以访问和复制,不可以修改
-Private 未经过允许的用户不能访问和复制以及修改

2.gitlab 需要自己公司大件
3.阿里云 腾讯 收费的私有仓库
4.gitee 码云 免费

1. 在本地添加一个远程仓库的地址
git remote add <仓库名称><仓库地址>
```shell
git remote add github https://github.com/378052182/text.git

# github 是仓库名称
# https://github.com/378052182/text.git 是仓库地址
```

2.  查询当前有哪些远程仓库
```shell
git remote
```

3. 删除远程仓库
git remote remove <仓库名称>
```shell
git remote remove github
```

4. 上传代码到远程仓库
git push <仓库名称> <分支名称>
```shell
git push github dev
```

5. 绑定默认分支
git push -u <仓库名称><分支名称>
```shell
# 第一次绑定
git push github dev
# 第二次提交
git push
```

testtest



