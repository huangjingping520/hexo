---
layout: post
title: axios 在 vue 项目中的全局配置
author: MerlinAlex
categories:
  - 前端
  - vue
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-03-15 21:32:50
tags:
  - 配置
description:
---

记录 vue 中 axios 的相关配置

<!-- more -->

在 vue 中如果在每个组件中都进行重复请求会非常的繁琐

可以在 `main.js` 中进行全局配置

```js
import axios from 'axios'

// 全局配置 axios 的请求根路径
axios.defaults.baseURL = '请求根路径'

// 把 axios 挂载到 Vue.prototype 上， 供每个 .vue 组件的实例直接使用
Vue.prototype.axios = axios
```

**缺点： 不利于API接口的复用**