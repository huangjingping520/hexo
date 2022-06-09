---
layout: post
title: .eslintrc
author: MerlinAlex
categories:
  - 前端
  - eslint
cover: false
music:
  server: netease
  type: song
  id: 536622304
date: 2022-06-09 15:24:50
tags:
  - 工具
  - eslint
description:
---

eslintrc

<!-- more -->

```json
{
  "extends": "@antfu",
  "rules": {
    "no-undef": "off",
    "comma-dangle": [
      "warn",
      "never"
    ],
    "@typescript-eslint/comma-dangle": "off",
    "arrow-parens": [
      "warn",
      "as-needed"
    ],
    "no-console": "off"
  }
}
```
