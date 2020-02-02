# GitHubTest  学习GitHub的使用
## 

Git Bash

### Git教程：
- [本文的git教程链接](https://blog.csdn.net/Hanani_Jia/article/details/77950594)
- [易百git教程](https://www.yiibai.com/git/git_add.html)

git-scm.com 首先进入GitHub官网，下载安装

首先要在本地创建一个ssh key 
  $ ssh-keygen-t rsa- C "注册GitHub的时候绑定的邮箱账号"
  需要输入这个代码，引号内需要改成你在注册GitHub的时候绑定的邮箱账号。
  之后会有一些简单的让你确认的操作，之后让你会提示操作路径、密码等等，
  一般情况下就直接按回车一路过就可以。
现在你就需要登录到你的GitHub上边添加这个密匙，打开你GitHub的设置界面，
找到SSH and GPG keys这个选项之后，在网页右上角有一个添加新的SSH keys,
这里的title 是让你给你的密匙起一个名字，根据个人喜好，什么名字都可以，
然后把你在刚刚文件中复制的密匙，填写在下边的大框里。保存即可。然后输入
<pre>$ ssh -T git@github.com</pre>，来检查是否成功绑定。
第一次绑定的时候输入上边的代码之后会提示是否continue，
在输入yes后如果出现了：You've successfully authenticated, but GitHub does not provide shell access 。
那就说明，已经成功连上了GitHub。接下来还需要简单的设置一些东西。
$ git config --global user.name "名字"
$ git config --global user.email "注册邮箱"
在网页版的GitHub新建库
在本地GitHub文件夹(定位到其他盘符:   cd /D)并进入这个文件夹，随便建一个文件

### 本地仓库与远程仓库合并                                             
1. git add命令将文件内容添加到索引(将修改添加到暂存区)。也就是将要提交的文件的信息添加到索引库中。
git add test.txt  
2. git commit命令用于将更改记录(提交)到存储库。将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中。//
git commit -m "the commit message" 
3. git push命令用于将本地分支的更新，推送到远程主机。它的格式与git pull命令相似。$ git push <远程主机名> <本地分支名>:<远程分支名>
git push origin master
4. 第一次的话会弹出一个登陆GitHub的输入框，登录即可
