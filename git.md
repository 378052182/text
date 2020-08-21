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
6. 克隆项目
在一台新设备上 完全没有项目的情况下 可以克隆(clone 复制)项目
git clone <仓库地址>
```shell
git clone  https://github.com/378052182/text.git
```
克隆的项目默认的远程仓库名称叫 origin(原始仓库)
远程仓库的地址 默认是当前克隆的地址

使用命令查看当前的仓库
git remote get-url <仓库名称>

```shell
#获取当前的仓库列表
git remote  => origin
# 获取当前仓库的地址
git remote get-url origin => https://github.com/378052182/text.git
```

-f 强制覆盖记录
不要在公司的项目中操作这个项目 否则你要被开除
```shell
git push -f
```

7. 同步远程仓库
拉取同步
git pull
```shell
git pull
```

在修改代码之前 先同步然后再修改
在提交代码到远程仓库的时候,如果本地和远程仓库不同步的话会报错

8. 下载主分支意外的其他分支
主分支已经克隆好了,想要下载dev开发分支
这里使用fetch

git fech <仓库名称> <远程分支名称>:<本地分支名称>中间使用冒号隔开
"远程分支名称"可以和"本地分至名称"不同名 建议使用相同的名称 免得项目管理起来混乱

```
git fetch github dev:dev
# github 是仓库名称
#第一个dev是远程仓库的dev分支代码
#第二个dev是下载到本地仓库时叫什么名字
```









