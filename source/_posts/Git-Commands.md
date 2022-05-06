---
layout: post
title: Git Commands
author: MerlinAlex
categories:
  - Git
  - 速查
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-05-04 22:51:47
tags:
  - Git
description:
---

Git 命令速查

<!-- more -->

`git branch`

显示分支列表，当前分支前有 `*`

```sh
* master
```

`git branch [branch-name]`

创建新分支

```sh
> git branch second

# git branch
* master
  second
```

`git checkout [branch-name]`

切换分支

```sh
> git checkout second
Switched to branch 'second'
```
