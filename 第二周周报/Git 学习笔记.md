

## Git 学习笔记

### Git 是什么

Git是目前世界上最先进的分布式版本控制系统，可以同git创建管理自己的文件，同时可以看到自己文件的修改时间和每次改动的地方

### 安装 Git 并创建版本库

在官网上安装，创建版本库需要指定一个特定的文件夹，使用

```git
git init
```

版本库表示这个目录中的所有文件都是可以被Git管理起来的，可以追踪每一个文件的改动

当然每次都将修改的文件提交给版本库进行管理，提交的方式为

```java
git add readme.txt //文件名，这是先把他提交给工作区
git commit -m 'wrote a readme file' // -m 后面是注释
```

### Git上可以查看和修改文件

```
cat readme.md //查看文件
git log // 查看修改的版本
git reset -- hard HEAD^ //回退上一个版本，HEAD中一个^表示回退一个版本
```

### Git上可以撤销自己的修改

```
git checkout -- readme.txt
```

命令`git checkout -- readme.txt`意思就是，把`readme.txt`文件在工作区的修改全部撤销，这里有两种情况：

一种是`readme.txt`自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是`readme.txt`已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

### Git 添加远程仓库

```
$ git remote add origin git@github.com:michaelliao/learngit.git
```

其中`git@github.com:michaelliao` 表示的是你要添加远程仓库的用户名 `learngit.git` 表示的是远程仓库中的仓库名

```
$ git push -u origin master
```

表示将自己的本地库中所有的文件推送到远程库上

### Git 从远程库中克隆

```
$ git clone git@github.com:michaelliao/gitskills.git
```

将远程库中的文件克隆到自己的本地库内

### Git 创建分支

分支表示你可以开创另一条线对文件进行修改，修改好后还可以将其与主线合并

```
git switch -c dev //这是创建和切换分支 dev是分支名
```





​	



