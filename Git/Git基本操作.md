[TOC]

---

# Mind[^ryf]

远程链接，需要本地创建ssh-key，存到对应平台中。接着链接远程git仓库，添加邮箱以及姓名。切换分支，最后同步。

git初始化

```bash
git init
## 直接初始化，此时分支名为master

git init {repo-name}
## 初始化新的文件夹，分支名为main

```



# git 嵌套仓库

如果仓库中有另一个嵌套仓库应该怎么同步？[^sub]

```bash
git submodule add {repo-link} {repo-git-name}
## repo-link即为子仓库链接
## repo-git-name，2025年2月8日，我理解的是git重命名本地时的索引，因为这样做才能正常提交。
```



# git显示本地仓库与远程名称

```bash
git remote -v
```

![image-20250211125512176](D:\AllTemp\坚果云\Typora\LearnProjects\Pictures\image-20250211125512176.png)



---

# Refer

[^sub]: http://jartto.wang/2017/12/28/cannot-nest-git-repository/
[^ryf]: https://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html

