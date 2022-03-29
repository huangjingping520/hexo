---
layout: post
title: JavaScript之闭包
author: MerlinAlex
categories:
  - JavaScript
  - 学习笔记
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-03-26 14:11:32
tags:
  - JavaScript
description:
---

JavaScript 之 闭包

<!-- more -->

> 闭包是指那些能够访问自由变量的函数。
> > 自由变量是指在函数中使用的，但既不是函数参数也不是函数的局部变量的变量。
> 闭包 = 函数 + 函数能够访问的自由变量

举例： 

```js
var a = 1
function fn () {
  console.log(a)
}
fn()
```

fn 函数可以访问到变量 a，但是 a 既不是 fn 函数的局部变量， 也不是 fn 函数的参数， 所以 a 就是自由变量。

于是， 函数 fn 加上 fn 访问的自由变量 a 就构成了一个闭包。

```js
var scope = 'global scope'
function checkscope() {
  var scope = 'local scope'
  function f() { return scope }
  return f
}

var fn = checkscope()
console.log(fn())
// local scope
```
