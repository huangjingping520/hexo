---
layout: post
title: oh-my-zsh
author: MerlinAlex
categories:
  - 工具
  - terminal
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2021-10-21 11:00:26
tags: 
  - 工具
  - 终端
description:
---

利用iTerms2和oh-my-zsh打造一套漂亮的终端系统

<!-- more -->

### 安装zsh

#### Ubuntu

```shell
sudo apt install zsh
# 设置为默认
chsh -s /bin/zsh
```

### macOS

macOS 高版本已经将默认shell从bash更换到了zsh

### 安装oh-my-zsh

可以使用curl或者wget

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

或者

```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### 安装Powerlevel10k

> 可以参照官网进行安装

```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

编辑`~/.zshrc`设置`ZSH_THEME="powerlevel10k/powerlevel10k"`

![image-20211003102644579](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003102644579.png)

### 安装Hack Nerd Font

```shell
git clone https://github.com/ryanoasis/nerd-fonts.git --depth 1
cd nerd-fonts
./install.sh
```

然后打开iterms2 到perferences或者Ubuntu Terminal设置字体

### 配置p10k

```shell
p10k configure
```

安装完p10k后会自动选择配置，可以按照上方命令再次设置，建议安装完自体后进行设置，否则或出现乱码

### macos中设置vscode Terminal

> 参考下方图片

![image-20211003104137867](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003104137867.png)