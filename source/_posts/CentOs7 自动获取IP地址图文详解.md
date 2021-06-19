---
title: CentOS7 自动获取IP地址图文详解
cover: https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619153039.png
tags: 
- CentOS
- CentOS7
---

环境: 
VMware workstation 12
CentOs7

当我们在VMware workstation 安装好CentOs后，IP地址默认不是自动获取的，如下图：
![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151648.png)



要设置CentOs7自动获取IP地址，需要进入系统网络配置文件夹，输入命令 ： “cd /etc/sysconfig/network-scripts/”，然后再输入 “ls” ,如下图所示：

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151714.png)

然后可以直接输入 “vi ifcfg-ens33” 进行修改，如下图 ：

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151736.png)

修改后如下：

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151804.png)

当然也可以直接输入 ： " vi /etc/sysconfig/network-scripts/ifcfg-ens33 " 进行编辑，如下图：

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151822.png)

修改完成后，“ :wq! ” 保存并退出，接下来就是重启网络服务咯，可以在根目录直接

输入“service network restart” 重启, 当然也有的人可能遇到有的CentOs版本

对“Service network restart”命令不起作用，但是我告诉还有一种方法，进入

到普通用户可以使用的命令的存放目录 “/bin”下，

再输入 " Systemctl restart network"，具体如下图：
![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151850.png)

注意，老版的Centos查看ip地址命令为 : " ipconfig -a " ,Centos7版本为 ： " ip addr " 

好了，修改完成后输入： " ip addr " ， 进行查看，如下图 : 

![](https://raw.githubusercontent.com/Oscargw/FigureBed/master/20210619151914.png)

