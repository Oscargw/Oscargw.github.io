---
title: 在Windows下编译QuickJS
date: 2021-11-18 17:00:04
tags:

- windows
- quickjs
- msys2
---

本文介绍如何在Windows下依赖MSYS2编译QuickJS。

## 安装MSYS2
这里我们采用清华大学镜像在Windows系统下安装MSYS2。

安装完成后，按照pacman配置配置好镜像源（参考镜像站说明）。

## 安装QuickJS环境
由于Windows下目前只支持32位系统编译，这里我们安装32位系统的编译环境

```shell
 pacman -S mingw-w64-i686-toolchain
 pacman -S mingw-w64-i686-dlfcn
 pacman -S make
```
至此完成了编译环境的配置

## 编译QuickJS
现在我们编译QuickJS，首先我们配置下Makefile中的

```makefile
prefix=/home/Administrator/quickjs
```
然后执行make install进行编译，完成编译后则在/home/Administrator/quickjs目录下看到quickjs相关的可执行文件。

## 常见问题
可以在[QuickJS中文Issues](https://github.com/quickjs-zh/QuickJS/pulls)中提出。

Page Index for this GitHub Wiki