---
title: 分享一个git 缩写脚本
date: 2020-07-20 14:41:35
categories: 
- Coding
tags:
- Github
---


![img](https://sponsor.segmentfault.com/lg.php?bannerid=0&campaignid=0&zoneid=25&loc=https%3A%2F%2Fsegmentfault.com%2Fa%2F1190000020350974%3Futm_source%3Dtag-newest&cb=8e3bc454ac)

> 分享一个git 缩写脚本

git 简写命令,加入linux,mac别名
使用方法:
./gsh [命令名] [参数,可选]

set 设置用户名和邮箱, 1:名称, 2:邮箱
init 设置git 简洁命令
gst: 代码变化状态,git status
gd: 查看当前代码改动变化, git diff, git diff 分支1 分支2
gam: [gam 备注] 代码提交本地仓库: git commit -am "备注"
gpu: [gpu 远程分支名] 与远程仓库关联: git push -u origin 分支名
gp: [gp]推送到远程仓库: git push
gl: [gl]拉取远程仓库代码:git pull
gb: [gb 新分支名]创建并切换新分支:git checkout -b 新分支名
gm: [gm 分支名]合并分支: git merge 分支名
gcm: [gcm 目标分支名]切换分支,并更新,再合并: git checkout 分支名B && git pull && git merge 分支名A
gsave 保存临时修改文件, git stash save
gpop 恢复临时修改的文件,git stash pop
glg 查看git日志.git log



```
#!/usr/bin/env bash
#
#
#
#                                                    __----~~~~~~~~~~~------___
#                                   .  .   ~~//====......          __--~ ~~
#                   -.            \_|//     |||\\  ~~~~~~::::... /~
#                ___-==_       _-~o~  \/    |||  \\            _/~~-
#        __---~~~.==~||\=_    -_--~/_-~|-   |\\   \\        _/~
#    _-~~     .=~    |  \\-_    '-~7  /-   /  ||    \      /
#  .~       .~       |   \\ -_    /  /-   /   ||      \   /
# /  ____  /         |     \\ ~-_/  /|- _/   .||       \ /
# |~~    ~~|--~~~~--_ \     ~==-/   | \~--===~~        .\
#          '         ~-|      /|    |-~\~~       __--~~
#                      |-~~-_/ |    |   ~\_   _-~            /\
#                           /  \     \__   \/~                \__
#                       _--~ _/ | .-~~____--~-/                  ~~==.
#                      ((->/~   '.|||' -_|    ~~-/ ,              . _||
#                                 -_     ~\      ~~---l__i__i__i--~~_/
#                                 _-~-__   ~)  \--______________--~~
#                               //.-~~~-~_--~- |-------~~~~~~~~
#                                      //.-~~~--\
#                               神龙保佑
#                              代码无BUG!
#
###########################################################################################################
# git 简写命令,加入linux,mac别名
```

# From: [分享一个git 缩写脚本](https://segmentfault.com/a/1190000020350974)