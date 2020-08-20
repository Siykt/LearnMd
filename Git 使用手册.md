# Git 使用手册

> init 初始化
>
> add 添加文件
>
> commit 提交文件

---

## init

**语法**： `$git init`

**功能：** 创建 Git 版本库，用于初始化 Git 仓库。

---

## add

**语法**： `$git add <File Name>`

**功能：** 添加/更新文件至暂存库。

---

## commit

**语法**： `$git commit -m <Commit Msg>`

**功能：** 提交更改。

---

## status

**语法**： `$git status`

**功能：** 查看仓库的所有修改状态的汇总与已提交暂存库修改过的文件。

---

## diff

**语法**： `$git diff <File Name>`

**功能：** 查看仓库具体文件的修改汇总。

---

## log

**语法**： `$git log <Options>`

**功能：** 查看 Git 当前版本库的提交、修改、创建分支、合并分支等相关日志。

**options：** [--pretty=oneline](www.baidu.com/s?wd=git%20log%20--pretty)

---

## reset

**语法**： `$git reset <Commit Id> <Options>`

**功能：** 回滚到指定版本。

**options：** [--hard](www.baidu.com/s?wd=git%20--hard)

---

## reflog

**语法**： `$git reflog`

**功能：** 查看所有的修改日志，包括回滚日志。

---

## checkout

**语法**： `$git checkout --<File Name>`

**功能：** 撤销文件的所有更改。

---

## rm

**语法**： `$git rm <file name>`

**功能：** 删除文件并添加修改到暂存库。

---

## remote

**语法**： `$git remote add <Origin Name> <Git E-mail>:<Origin Git Path>`

**功能：** 关联远程仓库。

---

## push

**语法**： `$git push <Origin Name> <Branch Name>`

**功能：** 提交文件至远程仓库。

---

## clone

**语法**： `$git clone <Git E-mail>:<Origin Git PatBh>`

**功能：** 克隆远程仓库。

---

## branch

**语法**： `$git branch <Branch Name>`

**功能：** 查看或创建分支。

---

## merge

**语法**： `$git merge <Branch Name>`

**功能：** 合并分支。

---
