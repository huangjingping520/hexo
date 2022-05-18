---
layout: post
title: vue and vite
author: MerlinAlex
categories:
  - vue
  - vite
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-05-17 23:01:27
tags:
  - demo
  - 练习
description:
---

a vue and vite demo

<!-- more -->

[代码地址](https://github.com/huangjingping520/vue3withVite)

# 搭建项目

```sh
npm init @vitejs/app
```

![](https://i0.hdslb.com/bfs/album/793202ec201d478175027f74567c3f65e57342db.png)

根据如上内容进行选择即可。

得到项目目录如下:

> ├── README.md
> ├── index.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;入口文件
> ├── package.json
> ├── public&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;资源文件
> │   └── favicon.ico
> ├── src&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;源码
> │   ├── App.vue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;单文件组件
> │   ├── assets
> │   │   └── logo.png
> │   ├── components   
> │   │   └── HelloWorld.vue
> │   └── main.js&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;入口
> └── vite.config.js&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vite工程化配置文件

使用 `pnpm install` 命令安装依赖

然后使用 `pnpm run dev` 启动项目，得到如下内容即表示成功。

![](https://i0.hdslb.com/bfs/album/66da74eda5c403a90064ad7bd1272eef2e7ab323.png)

使用 如下命令 安装 `vue-router` 和  `vuex`

```sh

pnpm add vue-routert vuex
```

# 规范

> ├── src
> │ ├── api 数据请求
> │ ├── assets 静态资源
> │ ├── components 组件
> │ ├── pages 页面
> │ ├── router 路由配置
> │ ├── store vuex数据
> │ └── utils 工具函数

# 引入路由

在 `router` 文件夹中新建 `index.js` 写入如下内容。

```js
import { createRouter, createWebHashHistory } from 'vue-router' 
import Home from '../pages/home.vue' 
import About from '../pages/about.vue' 
const routes = [ 
  { 
    path: '/', 
    name: 'Home', 
    component: Home 
  }, 
  { 
    path: '/about', 
    name: 'About', 
    component: About 
  } 
] 
const router = createRouter({ 
  history: createWebHashHistory(), 
  routes 
}) 

export default router
```

`createRouter` 新建路由实例

`createWebHashHistory` 配置内部使用 hash 模式的路由

然后在 `main.js` 中加载 router 的配置：

```js
import router from './router/index'

createApp(App).use(router).mount(''#app)
```
