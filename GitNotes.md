# Git and Github

#### 1.基本操作

初始化：

右键GitBah here打开后指令git init初始化本地仓库

设置签名：

项目级别/用户级别（一般用户，可以在本机系统上生效），优先度项目级>用户级别

```
项目级别：
git cobfig user.name [用户名]

git config user.email [邮箱]
用户级别：
git config --global user.name [用户名]
git config --global user.email [邮箱]
```

查看：cat.gitconfigsss

提交:

```
工作区 -git add [文件名]-> 缓存区 -git commit -m"注释"[文件名]-> 本地库
```

git status :查看提交情况

#### 2.版本操作

git log ：完整显示各个版本详细内容{b上翻页 ‘ ’ 下翻页}

git log --pretty=oneline 一行显示（详细）

git log --oneline 一行显示（粗略）

git reflog （荐）：一行显示（带版本号）



git reset --hard [版本号]:移动[HEAD]到[版本号]版本，刷新工作区 缓存区 本地库

git reset --mixed [版本号]: 移动[HEAD]到[版本号]版本，刷新缓存区 本地库

git reset --soft [版本号]:移动[HEAD]到[版本号]版本，刷新本地库

git reset~n 向之前版本回退n个版本

git reset^^ 向之前版本回退（n^) 个版本



注：若只是将删除提交到暂存区，版本号指定为HEAD即可找回

文件差异比较：

git diff [文件名]：工作区和暂存区文件比较

git diff [本地库历史版本] [文件名]：工作区文件和历史记录作比较([文件名]没有指定时比较全部文件)

#### 3.分支

创建分支：git branch [分支名]

查看分支：git branch -v

切换分支：git checkout[分支名]

合并分支：切换到接受修改的分支上git checkout[分支名]，使用git merge [分支名]

合并冲突解决：

<<<<<< HEAD 本分支

'>'>'>'>'>'>' 分支

进入文件解决后

git add--> git commit -m"[备注]" 结束合并状态（不能带文件名）
