# Sublime安装Package的3种方法
> Author : [Floyda](http://floyda.xyz/)  
> Date   : 2016-5-13  
> Github : https://github.com/Sublime-Chinese/sublime-zh  

[TOC]

### 1. Package Control 安装  

- [安装Package Control](./package_control.md).  
- 打开`command panel(Ctrl + Shifht + P)`, 输入`pci`.  
- 等待Package列表返回.  
- 选择并回车安装.  

### 2. Git Clone 安装  

- 在Github上搜索, 找到合适的Package.  
- 命令行cd到[Package Path](./packages_path.md), `Git Clone`到当前路径.  

### 3. Zip 安装  

- Github上有个``Download ZIP`, 点击下载.  
- 解压到[Package Path](./packages_path.md).  

### 三种方式的优劣

- Package Control 安装  
    - 方便
    - 现在流行压缩成`.sublime-package`, 速度快, 不过查看源码和修改都比较麻烦.  
    - 没有详细介绍, 只能根据名字, 猜一下这个Package大概是干什么, 如果搜索结果不多, 都可以安装体验一下.  
    - 最好的办法是到[Package Control的官网](https://packagecontrol.io/)去搜索, 看完介绍在决定安装哪一个.  

- Git Clone 安装  
    - 要求会使用Git, 除此之外, 好处多多, **五星推荐**.  

- Zip 安装  
    - 众所周知的原因, 网络不通的时候, 可以问其他人拿一个Zip包.  
    - 适合非程序员使用.  