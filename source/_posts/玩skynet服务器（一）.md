---
title: 玩skynet服务器（一）
cover: https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210608142546.png
tags: 
- skynet
---

## 文章

- [Home](https://github.com/cloudwu/skynet/wiki)
- [GettingStarted](https://github.com/cloudwu/skynet/wiki/GettingStarted)
- [社区](https://github.com/cloudwu/skynet/wiki/Community)

skynet，github链接：
https://github.com/cloudwu/skynet/

### 实操踩坑

```shell
# git clone https://github.com/cloudwu/skynet.git
# 替换为cnpmjs.org:
git clone https://github.com.cnpmjs.org/cloudwu/skynet.git
cd skynet
make 'linux' # make 'PLATFORM'  # PLATFORM can be linux, macosx, freebsd now
```

- 提示报错：

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210608142947.png)

缺少make。解决方法 - 运行安装make命令：

```shell
yum install gcc automake autoconf libtool make
```



- 提示报错：

```shell
autoconf: command not found

# 解决方法：
yum install autoconf
```

