# Packages Path
> Author : [Floyda](http://floyda.xyz/)
> Date   : 2016-5-13
> Github : https://github.com/Sublime-Chinese/sublime-zh

[TOC]

Sublime有2个`Packages Path`

## 安装路径下的Package  
Sublime启动的时候, 首先加载这里面的`.sublime-package`文件(可以被重载)

- Windows
    `Ex: D:\Sublime Text 3\Packages`
- Mac
    `Ex: `
- Linux
    `Ex: `


## AppData下的Package  
作为插件来加载的Packages, 可以被`Package Control`来管理.

- Windows
    `Ex: C:\Users\Administrator\AppData\Roaming\Sublime Text 3\Packages`
- Mac
    `Ex: `
- Linux
    `Ex: `

可以通过Sublime里的菜单`Preference->Browse Packages...`打开文件夹位置.


## 为什么自定义的`设置`和`快捷键`要写在User里面, 而不能写在Default?

Sublime升级的时候, 会将整个安装路径下的东西覆盖一遍, 所以写在`Settings Default`或者`Key Bindings Default`里面的东西, 当前版本是OK, 一旦升级, 全部还原.  
根据加载顺序, 写在`User`里面的东西, 不管`Default`怎么写, 启动的时候都会重载. 所以, 别在`Default`里面改东西(后面作者加了读写权限).

