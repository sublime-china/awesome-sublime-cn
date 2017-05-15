---
title: 在Mac上搭建C#的Sublime开发环境
date: 2017-05-10
tags: [Sublime]
categories: Sublime
---

> [各语言编译环境](http://www.jianshu.com/p/3e25fcf7600e)


## 安装Mono
- 下载并安装 - [传送门](http://www.mono-project.com)
- 新建'test.cs'文件

```cs
using System;

public class HelloWorld
{
    static public void Main ()
    {
        Console.WriteLine ("Hello Mono World");
    }
}
```

- 测试

```shell
mcs test.cs
mono test.exe
# Hello Mono World
```

## C#的Sublime开发环境
- 在'~/Library/Application Support/Sublime Text 3/Packages/User/'中新建一个文件'cs.sublime-build'

```
{
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.cs",
    "shell":true,
    "windows":
        {
            "cmd": ["to be continue"],
        },
    "linux":
        {
            "cmd": ["to be continue"],
        },
    "osx":
        {
            "cmd": ["rm -f ${file_path}/${file_base_name}.exe; /usr/local/bin/mcs ${file}; /usr/local/bin/mono ${file_path}/${file_base_name}.exe"],
        }
}
```
其中'/usr/local/bin/mcs'和'/usr/local/bin/mono'修改成自己机子的环境变量
可以通过`where`得到
```
where mcs
where mono
```

- 打开`.cs`文件, `command + shift + B`选择build的配置文件, 以后直接`command + B`即可在Sublime中编译并显示C#文件的结果.

