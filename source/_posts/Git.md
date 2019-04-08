---
title: Git
date: 2019-04-08 21:01:38
tags:
---
创建空分支
```bash
git checkout --orphan <BRANCH_NAME>
```

更新远程分支列表
```bash
git remote update origin --prune
git remote update origin -p
```

删除本地分支
```bash
git branch -d BRANCH_NAME
```
删除远程分支
```bash
git push origin -d BRANCH_NAME
git push origin --delete BRANCH_NAME
```

新增本地分支
```bash
git branch BRANCH_NAME
```
切换本地分支
```bash
git checkout BRANCH_NAME
```
新增并切换分支（本地）
```bash
git checkout -b BRANCH_NAME
```