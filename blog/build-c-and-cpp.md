---
title: 搭建Sublime的C/C++开发环境
date: 2017-05-15
tags: [Sublime]
categories: Sublime
---

> [各语言编译环境](http://www.jianshu.com/p/3e25fcf7600e)


- 确认gcc已经安装

- 在`Packages/User`目录下新建文件`cpp.sublime-build`

```
{
    "cmd" : ["gcc ${file} -o ${file_path}/${file_base_name}; ${file_path}/${file_base_name}"],
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c, source.c++",
    "shell": true
}
```
