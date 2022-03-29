---
layout: post
title: JavaScript之继承
author: MerlinAlex
categories:
  - JavaScript
  - 学习笔记
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-03-26 13:37:59
tags:
  - JavaScript
description:
---

记录JavaScript各种继承的方法和优缺点

<!-- more -->

## 原型链继承

```js
function Parent () {
  this.name = 'parent'
}

Parent.prototype.getName = function () {
  console.log(this.name)
}

function Child () {}

Child.prototype = new Parent()

var child = new Child()

console.log(child.getName())
```

```sh
parent
```

**缺点：**

1. 引用类型的属性会被所有实例共享
2. 在创建Child的实例时，不能像Parent传参


## 经典继承（借用构造函数）

```js
function Parent () {
  this.names = ['Kevin','David']
}

function Child () {
  Parent.call(this)
}

var child1 = new Child()

child1.names.push('Tom')

console.log(child1.names) //['Kevin','David','Tom']

var child2 = new Child() 

console.log(child2.names) //['Kevin','David']
```

**优点：**

1. 避免了引用类型的属性被所有实例共享
2. 可以在Child中向Parent传参

```js
function Parent (name) {
  this.name = name
}

function Child (name) {
  Parent.call(this, name)
}

var child1 = new Child('Kevin')

console.log(child1.name) //Kevin

var child2 = new Child('David')

console.log(child2.name) //David
```

**缺点：**

方法都在构造函数中定义，每次创建实例都会创建一遍方法。

## 组合继承

结合了原型链继承和经典继承

```js
function Parent (name) {
  this.name = name
  this.colors = ['red','blue','green']
}

Parent.prototype.getName = function () {
  console.log(this.name)
}

function Child (name, age) {
  Parent.call(this, name)
  this.age = age
}

Child.prototype = new Parent()
Child.prototype.constructor = Child

var child1 = new Child('Kevin', '18')

child1.colors.push('black')

console.log(child1.name) //Kevin
console.log(child1.age) //18
console.log(child1.colors) //['red','blue','green','black']

var child2 = new Child('David', '20')

console.log(child2.name) //David
console.log(child2.age) //20
console.log(child2.colors) //['red','blue','green']
```

**优点：**

结合了原型链继承和构造函数的优点，是JavaScript中最常用的继承模式

