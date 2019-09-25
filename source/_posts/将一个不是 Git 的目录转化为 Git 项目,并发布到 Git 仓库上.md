---
title: 将一个不是 Git 的目录转化为 Git 项目,并发布到 Git 仓库上
date: 2019-09-25 17:15:44
tags: Git
---

### 1. 打开命令行终端，进入项目所在的本地目录，将目录初始化为一个 Git 项目:

```
$ git init
// 此时会在目录中创建一个 .git 隐藏文件夹
```

### 2. 将所有文件放进新的本地 Git 仓库:

```
$ git add .
/**
* 如果你本地已经有 .gitignore 文件，
* 会按照已有规则过滤不需要添加的文件。
* 
* 如果不想要添加所有文件，
* 可以把 . 符号换成具体的文件名
*/
```
	
### 3. 将添加的文件提交到仓库:

```
$ git commit -m "init project"
```

### 4. 在 Git 服务器上创建一个空的新仓库，为了避免冲突，不要创建任何文件，例如 **README** 也不要创建.

### 5. 复制仓库地址，在命令行中关联仓库地址:

```
$ git remote add origin https://github.com/xxx/xxx.git
	
// 可运行以下命令查看关联结果：
$ git remote -v
```

### 6. 提交代码到 Git 仓库:

```
$ git push origin master
```
