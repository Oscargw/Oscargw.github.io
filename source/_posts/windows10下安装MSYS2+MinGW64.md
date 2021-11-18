---
title: windows10下安装MSYS2+MinGW64
date: 2021-11-18 16:00:04
tags:
- win10
- msys2
- mingw
---

1. 下载msys2，官方地址：http://www.msys2.org/，这里选择64位的安装器

2. 安装完成之后，先别启动msys2，在 安装根目录/etc/pacman.d/ 下找到mirrorlist.mingw32、mirrorlist.mingw64和mirrorlist.msys并进行修改。

mirrorlist.mingw32文件添加一行，Server = http://mirrors.ustc.edu.cn/msys2/mingw/i686/

mirrorlist.mingw64文件添加一行，Server = http://mirrors.ustc.edu.cn/msys2/mingw/x86_64/

mirrorlist.msys文件添加一行，Server = http://mirrors.ustc.edu.cn/msys2/msys/$arch/

3. 在win10菜单中找到MSYS 64bit并启动MSYS2 MinGW 64-bit

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20211118160327.png)
![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20211118160342.png)

4. 认识下命令

pacman -Syu => 同步软件库并更新系统到最新状态

pacman -S package_name1 package_name2 => 安装或者升级单个软件包，或者一列软件包（包含依赖包）

pacman -R package_name => 删除单个软件包

pacman -Rs package_name => 删除指定软件包，及其所有没有被其他已安装软件包使用的依赖关系

5. 输入pacman -Syu 更新软件库, 完结后直接点击关闭按钮来关闭窗口

6. 重新来一次第2个步骤(这个时候因为更新软件库的原因导致第2个步骤里面的三个文件被覆盖了)

7. 使用命令安装mingw64等必要的软件(一个一个地安装)

pacman -S gcc

pacman -S mingw-w64-x86_64-toolchain

pacman -S mingw-w64-i686-toolchain

pacman -S mingw-w64-x86_64-SDL2

pacman -S mingw-w64-i686-SDL2

pacman -S base-devel

pacman -S vim

pacman -S yasm

pacman -S nasm

pacman -S make

