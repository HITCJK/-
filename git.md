# Git常用命令
- [配置](#配置)
- [搭建本地仓库](#搭建本地仓库)
- [版本管理](#版本管理)
- [分支(咱学生一般用不着)](#分支咱学生一般用不着)
- [远程仓库](#远程仓库)

## 配置
>`git config`
>
>>`--system` #系统配置
>>
>>`--global` #全局配置
>>
>>`-l --list` #查看配置

使用git前需要配置用户的姓名和邮件信息(不需要真实,写了就行)

>`git config --global user.name 'yourname'`
>
>`git config --global user.email 'youremail'`

## 搭建本地仓库

>`git init` #初始化本地仓库
>
>`git status` #查看仓库中的文件状态
>
>`git diff` #查看更新的详细信息，与git status不同的是，git status只显示更新的状态，而 git diff 可以显示已写入缓存与已修改但尚未写入缓存的改动的区别具体的详细信息。(其实一般用status就行)
>
>`git add <filename>` #将更改添加到暂存区(可使用通配符"."添加全部文件,使用"*.扩展名"添加一类文件)
>
>`git checkout – <filename>` #放弃未暂存文件修改
>
>`git rm --cached <filename>` #删除暂存区的文件(且此后不再跟踪,不再提示未暂存)
>
>`git reset HEAD <filename>` #将文件回退到最后提交的版本(放弃修改)
>
>`git commit -m <message>` #提交到本地仓库 -m:添加提交信息(就算你这会儿不添加也会让你再写🤡)
>
>>`-a` #将被修改的文件暂存并提交

## 版本管理

>`git log` #查看历史版本
>
>`git reflog` #简化版历史版本
>
>>`--online` #简洁历史版本
>
>`git reset --hard <版本号>` #重置到该版本

## 分支(咱学生一般用不着)

>`git branch` #查看分支
>
>`git branch <branchname>` #新建分支
>
>`git checkout <branchname>` #切换分支
>
>>`-b`创建新分支并立即切换到该分支下
>>`–graph` #查看历史中什么时候出现了分支、合并
>>`–reverse` #逆向显示所有日志
>
>`git branch -d <branchname>` #删除分支
>
>`git merge <branchname>` #将任意分支合并到到当前分支中去

## 远程仓库
>`git push <url> <branch>` #将当前分支提交到远程仓库的branch分支
>
>`git clone <url>` #将远程仓库克隆到本地
>
>`git pull <url>` #拉取远程仓库同步到本地
>
>`git fetch <url>` #抓取远程仓库,该命令执行完后需要执行git merge 远程分支到你所在的分支,实际一般用pull一步到位
>
>`git remote add <alias> <url>` #为远程仓库地址设置别名
>
>`git remote` #查看已有的别名
>
>>`-v` #详细信息
>
>`git remote rm <alias>` #删除远程仓库别名