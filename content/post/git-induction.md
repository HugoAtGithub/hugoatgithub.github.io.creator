---
title: "Git Induction"
date: 2020-06-22T00:02:48+08:00
draft: true
---

#### Git 入门

##### git 四行配置

```bash
git config --global user.name 你的英文名
git config --global user.email 你的邮箱
git config --global push.default simple
git config --global core.quotepath false
```

> [git 运行配置](https://www.jianshu.com/p/f29ca723db4f) 的一些技巧

##### 常用操作

- git add 选择要提交的内容
- .gitignore 文件描述不提交的内容
- git commit -V 用来提交
- git log 用来查看历史
- git reset --hard XXXXX 用来御剑飞行切换版本
- git reflog 用来查看所有历史
- git branch x
- git checkout x
- git merge x



#### Git 远程仓库

##### 生成 ssh key

```shell
ssh-keygen -t rsa -b 4096 -C 你的邮箱
cat ~/.ssh/id_rsa.pub                           # 得到公钥内容
ssh -T git@github.com
git remote add origin git@xxxxxxx
git push -u origin master
```



##### 远程仓库操作命令

- git pull  拉取代码
- git push  上传代码
- git clone  克隆项目
- git remote add origin git@xxxx   在本地添加远程仓库地址



##### 高级操作

```shell
touch ~/.bashrc
echo 'alias ga="git add"'>> ~/.bashrc
echo 'alias gc="git commit -v"'>> ~/.bashrc
echo 'alias gl="git pull"'>> ~/.bashrc
echo 'alias gp="git push"'>> ~/.bashrc
echo 'alias gco="git checkout"'>> ~/.bashrc
echo 'alias gst="git status -sb"'>> ~/.bashrc
```

最后 code ~/.bashrc 在文件最后加上

```shell
alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit -- | less"
```



##### 其他 Git 操作

- git rebase -i xxxx  美化历史命令
- git rebase --abort 取消rebase
- git rebase --continue 继续
- git stash / git stash pop

