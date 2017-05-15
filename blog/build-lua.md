---
title: 搭建Sublime的Lua开发环境
date: 2017-05-15
tags: [Sublime]
categories: Sublime
---

> [各语言编译环境](http://www.jianshu.com/p/3e25fcf7600e)


- 确认已经安装Lua

- 在`Packages/User`目录下新建文件`Lua.sublime-build`
```
{
    "cmd": ["/usr/local/bin/lua", "$file"],
    "file_regex": "^(?:lua:)?[\t ](...*?):([0-9]*):?([0-9]*)",
    "selector": "source.lua",
    "encoding": "utf-8",
    "shell": true
}
```