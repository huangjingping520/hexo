---
layout: post
title: clash for Ubuntu
author: MerlinAlex
categories:
  - 工具
  - 网络
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2021-10-21 11:04:58
tags: 
  - 工具
  - clash
  - web
description:
---

在Ubuntu系统下安装配置clash。
声明：本文章只做技术探讨，不要利用本文章提及的技术做违反法律的事情。

<!-- more -->

## 设备

Ubuntu 20.04.2 for linux from Parallels Desktop

## 安装过程

1. 打开Ubuntu文件管理器

   ![image-20211003095951415](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003095951415.png)

2. 在Home目录下新建clash文件夹

   ![image-20211003100106386](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003100106386.png)

3. 打开firefox浏览器

4. 输入https://github.com/Dreamacro/clash/releases并访问

5. 找到最新的版本并根据自己的系统选择相应文件下载

   ![image-20211003100448505](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003100448505.png)

6. 保存文件后双击点击提取到clash文件夹下并改名clash

   ![image-20211003100604074](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003100604074.png)

7. 打开terminal进入clash文件夹然后输入`wget -O config.yaml 订阅地址?clash=1&log-level=info`命令，会生成两个新文件

   ![image-20211003100822078](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003100822078.png)

8. 在terminal中输入以下内容启动

   ```shell
   ./clash -d .
   如果提示权限不够(permission deny)，则输入chmod +x clash
   再输入./clash -d .
   ```

9. 在浏览器打开http://clash.razord.top/#/proxies

   ![image-20211003101139322](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003101139322.png)

10. 打开setting，点击该位置

    ![image-20211003101231533](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003101231533.png)

11. 设置为手动并将相应代理位置填写一致

    ![image-20211003101436595](https://gitee.com/merlinalex/pic-go/raw/master/image-20211003101436595.png)