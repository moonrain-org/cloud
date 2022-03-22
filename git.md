git 三大区域

- 工作区

- 暂存区

- 版本库

回滚

```
git reset --hard  版本号
git log 可查看版本号
git reflog 可查看所有版本号，包括回滚之前的版本号
```

分支

```
git branch 查看分支
git branch dev 创建新分支
git checkout dev 切换分支
git branch -d 分支名称 删除分支
git merge 要合并的分支
注意： 切换分支再合并
```



```
1.给远程仓库起别名
git remote add origin 远程仓库地址
2.向远程推送代码
git push -u origin 分支
```

```
1.克隆远程仓库代码
git clone 远程仓库地址
2.切换分支
git checkout 分支
```

```
1.拉取远程仓库代码
git pull origin 分支名称
```



