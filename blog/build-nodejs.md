---
title: 搭建Sublime的Nodejs开发环境
date: 2017-05-15
tags: [Sublime]
categories: Sublime
---

> [各语言编译环境](http://www.jianshu.com/p/3e25fcf7600e)


- 安装Node.js

- 在`Packages/User`目录下新建文件`Nodejs.sublime-build`
```
{
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.js",
    "shell":true,
    "windows":
        {
            "cmd": ["taskkill /F /IM node.exe; node $file"]
        },
    "linux":
        {
            "cmd": ["killall node >/dev/null 2>&1; node $file"]
        },
    "osx":
        {
            "cmd": ["killall node >/dev/null 2>&1; node $file"]
        }
}

```

