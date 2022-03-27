git 三大区域

- 工作区

- 暂存区

- 版本库

```
1.执行初始化命令
git init
2.管理目录下的文件状态
git status
注：新增的文件和修改过后的文件都是红色
3.管理指定文件夹（红变绿）
git add 文件名
git add .
4.个人信息配置：用户名、邮箱【一次即可】
git config --global user.email 'you@example.com'
git config --global user.name 'Your Name'
5.生成版本
git commit -m '描述信息'
```

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

等同于
git fetch origin dev
git merge origin/devs

```

rebase （变基）一 使代码提交记录变得简洁

```
git rebase -i HEAD~3  合并当前位置最近的3条记录

合并记录时尽量不要合并push到远程仓库的提交记录
```

```
git log --graph  图形化查看日志
git log --graph --pretty=format:"%h %s" 简洁图形化查看日志

dev分支
git rebase master
切换master
git checkout master
合并dev分支
git merge dev

```

快速解决冲突

```
1.安装beyond compare
2.在git中配置
git config --local merge.tool bc3
git config --local mergetool.path "C:\Program Files\Beyond Compare 4\BCompare.exe"
git config --local mergetool.keepBackup false
3.应用beyond compare 解决冲突
git mergetool
```

gitflow工作流思路

```

```

创建组织项目

```
git tag -a v1 -m '第一版' 为提交记录打上标签
git push origin --tags 把标签推送到远程仓库

git checkout -b dev 创建dev分支并切换到dev分支
```

给开源软件贡献代码

```
1、fork源代码
将别人源代码拷贝到自己的远程仓库
2、在自己仓库进行修改代码
3、给源代码的作者提交 修复bug的申请（pull request）
```

配置文件存放的3个位置

```
1、项目配置文件
项目/.git/config
git config --local user.name 'tutao'
2、全局配置文件
C:\Users\ttao\.gitconfig
git config --global user.name 'tutao'
3、系统配置文件
C:\Program Files\Git\etc\.gitconfig
git config --system user.name 'tutao'
注意：需要有root权限
```

应用场景:

```
git config --local user.name 'tutao'
git config --local user.email 'tutao@xx.com'

git config --local merge.tool bc3
git config --local mergetool.path "C:\Program Files\Beyond Compare 4\BCompare.exe"
git config --local mergetool.keepBackup false

git remote add origin地址，默认添加在本地配置文件中（--local）
```

免密码登录

```
1、URL中体现
原来的地址：https://github.com/ttao857/dbhot1.git
修改的地址：https://用户名:密码@github.com/ttao857/dbhot1.git

git remote add origin https://用户名:密码@github.com/ttao857/dbhot1.git

2、SSH实现
生成公钥和私钥(默认放在C:\Users\ttao\.ssh)根目录下 id_rsa.pub公钥，id_rsa私钥
ssh-keygen
拷贝公钥内容，并在github设置中添加
在git本地中配置ssh地址
git remote add origin git@github.com:ttao857/dbhot1.git
以后使用
git push origin master 不需要密码

git自动管理凭证
```

git 忽略文件

```
让git不在管理当前目录下的某些文件
*.h
!a.h
files/
*.py[c|a|d]
更多参考 https://github.com/github/gitignore
```

GitHub任务管理相关

```
issues 文档以及任务管理

wiki项目文档说明
```







