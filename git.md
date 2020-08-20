## git上传包提交时出现：Please tell me who you are.
```
解决方法：在命令行中执行
git config --global user.email "你的邮箱"
git config --global user.name "你的名字"

输入完后再接着执行git commit "注释"
```